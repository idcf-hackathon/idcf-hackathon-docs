# DevOps 黑客马拉松

IDCF黑客马拉松以【园丁之家】作为商业背景，提供了从商业模式创意，用户画像，故事地图，迭代规划，Kanban管理，持续交付流水线搭建，产品原型创建到商业路演的端到端实战演练。

## 园丁之家技术架构指引

专注于健康绿色生活，为现代都市人提供搭建个人专属花园的垂直电商。2016年初启动，2017年6月获得天使投资，2018年6月A轮后开始盈利，当前实现5000万用户，日活200万，日销售额GMV 1亿元，亚马逊已有收购意向。

### 技术架构

TailwindTraders后台应用使用了以下应用组件提供一套微服务架构的应用模型，运行在微软云Azure平台之上。

- 后端系统
  - 代码库 <https://github.com/idcf-hackathon/TailwindTraders-Backend>
    - A组：<https://github.com/idcf-hackathon/TailwindTraders-Backend-HackA>
    - B组：<https://github.com/idcf-hackathon/TailwindTraders-Backend-HackB>
    - C组：<https://github.com/idcf-hackathon/TailwindTraders-Backend-HackC>
  - [后端系统部署操作手册](docs/backend/README.md)

- 前端系统
  - 代码库 <https://github.com/idcf-hackathon/TailwindTraders-Website>
    - 各小组自行fork到自己的Github账号中
  - [前端系统部署操作手册](docs/website/README.md)

### 当前生产环境入口

<https://td.devopshub.cn/>

## DevOps工具链

全部采用微软Azure DevOps平台管理从需求，项目，任务，看板，代码和流水线的端到端持续交付流水线。

- Azure DevOps 入口 <https://dev.azure.com>
- Azure 云管理控制台入口 <https://portal.azure.com>

@IDCF
