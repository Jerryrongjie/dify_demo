# dify_demo
It's a demo app built by dify.

通过Dify搭建的工作流、Agent应用。

## 介绍
### CoT Chatflow
通过模仿o1 CoT（Chain of Thought）模式，进行 Agent Workflow搭建，步骤式的进行问题分析、任务拆解、任务执行、推理总结等步骤，更好地完成用户需求，提高回答的可靠性。

本Demo仅通过多LLM节点编写Prompt的方式进行模拟，不代表o1的真实逻辑，仅作为学习参考。

![Chatflow_demo](https://github.com/user-attachments/assets/208c0392-461b-4312-b179-ba1435271baa)

项目体现了Agent的四个核心能力：
1. 感知能力：支持使用视觉模型，提供多模态感知能力。
2. 规划能力：支持由大模型自行规划问题的解决步骤并拆分为任务项。
3. 执行能力：通过获取大模型自行规划的任务，完成任务的处理并生成处理结果。
4. 自我反思：结合原始提问、任务步骤完成结果进行内容的汇总整合，并输出完整的推理过程、结论。

![Chatflow_config](https://github.com/user-attachments/assets/5f06764a-c5d0-4672-beba-09a3f59dc926)

### 36kr | daily news
查询36kr官方内容号发布的每日新闻汇总，并通过jina.ai的接口服务获取新闻内容转为Markdown格式。

1. 通过接口查询36kr每日新闻汇总"8点1氪"的最新内容。
2. 使用Python代码提取所需的文章参数，转为迭代器可用的Array结构。
3. 使用迭代器，查询目标文章正文内容并转为可读性较强的Markdown语法内容。
	1. 获取文章id参数`ItemId`。
	2. 通过Jina.ai接口，获取1.提供的文章id的正文内容并转为Markdown格式。
4. 对迭代内容进行整合。
5. 输出工作流结果。

![image](https://github.com/user-attachments/assets/fc619073-6b2a-4fc7-9ae8-668673e45b96)


## 如何使用
### 前提条件
1. 项目基于 Dify 0.14.1版本进行搭建，请使用不低于该版本的Dify服务。
2. 需要提前部署社区版Dify 或 申请Dify.ai账号进行体验。

### 使用流程
1. 下载仓库dsl目录中的yml文件。
2. 访问本地dify服务或cloud.dify.ai，完成登录。
3. 访问"Studio/工作室"，在左上角第一个卡片中，点击"Import DSL file/导入DSL文件"，完成yml文件上传。
4. 点击已上传的APP即可进行编辑。

![image](https://github.com/user-attachments/assets/1d0b0f18-6aad-4145-b25f-31279bf14ab9)

## 说明
本项目基于Dify进行搭建，仅供学习与参考。
