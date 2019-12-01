# IDCF 黑客马拉松示例项目 TailwindTraders 后台应用

TailwindTraders后台应用使用了以下应用组件提供一套微服务架构的应用模型，运行在微软云Azure平台之上。

![azure resource group](/Documents/Images/hack/azure-resource-group.png)

## 组件列表/项目结构

- 以下应用组件采用微服务应用架构，运行于Azure Kubernetes Service
  - /Source/ApiGWs/
    - Tailwind.Traders.WebBff：web端应用网关，提供网站对于后端服务环境的访问入口
    - Tailwind.Traders.Bff：手机端应用网关，提供iOS/Android应用对于后端应用的访问入口
  - /Source/Services/
    - TailwindTraders.Cart.Api: 购物车应用服务
    - TailwindTraders.Congnitive.Docker：AI认知服务，提供针对图片的人工智能识别服务，用于根据用户上传图片自动搜索商品
    - TailwindTraders.Coupon.Api: 代金券服务
    - TailwindTraders.ImageClassifier.Api: 图片识别服务，通过调用AI认知服务完成图片识别
    - TailwindTraders.Login.Api: 用户登录认证服务
    - TailwindTraders.PopularProduct.Api: 流行商品服务
    - TailwindTraders.Product.Api: 商品品类服务
    - TailwindTraders.Profile.Api: 用户个人资料服务
    - TailwindTraders.Stock.Api: 商品库存服务
- 以下应用组件使用Azure云PaaS服务提供
  - 无服务计算(Serverless) Azure Funciton
    - /Source/Services/TailwindTraders.Visits.Function: 用户访问统计服务
  - 托管的PostgreSQL数据库服务
    - stockdb: TailwindTraders.Stock.Api的后台数据库
  - 托管的NoSQL数据库服务 CosmosDB
    - MongoDB兼容模式：TailwindTraders.Coupon.Api: 代金券服务数据库
    - CosmoDB原生模式：TailwindTraders.Cart.Api: 购物车应用服务数据库
  - 托管的SqlServer数据库服务
    - TailwindTraders.PopularProduct.Api: 流行商品服务数据库
    - TailwindTraders.Product.Api: 商品品类服务数据库
    - TailwindTraders.Profile.Api: 用户个人资料服务书库
  - 对象存储服务 Azure Storage
    - 提供商品图片的高性能持久化存储以及CDN服务
- 应用使用性能分析(APM)，监控以及日志服务使用Azure云PaaS服务提供
  - 容器监控解决方案服务 Container Insight
  - 日志及分析服务 Log Analytics工作区
- Docker镜像仓库服务使用Azure云PaaS服务提供
  - 容器注册表服务
