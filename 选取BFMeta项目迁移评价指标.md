
# 选取BFMeta项目迁移评价指标 - 项目选择标准指南
*v0.0.2*

## 制定迁移项目选择指标目的
- 避免因项目组经验不足，选取低质量的项目进行迁移
- 避免选取功能性不全项目
- 避免选取产品功能性单一，无创新性项目
- 避免团队成员技术栈不能匹配所选迁移项目使用的技术栈造成进度阻塞
本指南按照所选迁移项目的代码功能完整性、代码实现完整性、项目质量、产品性、技术栈等多个维度对项目进行综合评分，力争多维度客观的进行评估所迁移的项目。

## 使用指南
按照细则对所迁移项目进行多维度的打分，每个维度满分10分，标准权重20%（可以根据每个团队的实际情况，适当的修改每项的权重），对所有维度进行加权平均，最终得出总分，并按照下标进行评估：
|  分数范围   | 评估结果  |
|  :-:  | :-:  |
| >=9分  | 优秀项目，建议迁移 |
| >=6分  | 可以进行迁移 |
| <6分  | 劣质项目，不建议进行迁移 |

## 细则
### 1.代码功能完整性（满分10分）
评分标准：代码是否实现了该类型应用的相应功能，并且都是在链上进行交互，按照功能的上链程度以及常用功能是否完整两个方面进行评估:
- 所有功能上链百分率（满分5分）：100%（5）大于80%（4）大于60%（3）大于40%（2）大于20%（1）

- 常用模块（如NFT模块）是否完整（满分5分 加分项）：具有相关功能进行加分，都没有得0分
	- 用户模块 +1分
	
	- 链上交易模块 +2分 
	
	- 链上资产模块 +2分 
	
	  --
	
	  溯源
	
	  

### 2.代码实现完整性（满分10分）
评分标准：对代码实现的完整性进行评估，主要侧重于技术层面，加分项，满足则加对应选项的分数
- 导入BFMeta是否可编译 3分
- 是否可运行 3分
- 前后端代码齐全 1分
- 数据存储方式（采用数据库）1分
- 是否有部署性脚本 1分
- 可扩展性  1分

### 3.项目质量（满分10分）
评分标准：所选项目的质量进行评估，按照开源项目的喜爱程度及维护工薪程度两个方面进行评估，两项分数相加
- issues解决周期&&更新频率(满分5分）: 
|  更新频率  | 得分  |
|  :-:  | :-: |
| 月  | 5 |
| 季度  | 4 |
| 半年  | 3 |
| 年  | 2 |
| >1年  | 1 |

- star数量（满分5分）: 
|  star数量  | 得分  |
|  :-:  | :-:  |
| >1000+  | 5 |
| >500+  | 4 |
| >100+   | 3 |
| >50+  | 2 |
| >10+  | 1 |

### 4.产品性评估（产品主观评估）（满分10分）
评分标准：此维度较为抽象主观，目前没有找到好的评分标准，以下标准仅供参考，五个维度分数相加
- UI设计（满分2分）:
|  标准 | 得分  |
|  :-:  | :-:  |
| 较粗糙 | 0 |
| 一般 | 1 |
| 惊艳   | 2|

- 用户体验（满分2分）: 卡顿，不符合，一般1分，惊艳2分
|  标准 | 得分  |
|  :-:  | :-:  |
| 较差，反人类直觉 | 0 |
| 一般 | 1 |
| 优秀，流畅  | 2|

- 市场需求度，实用性（满分2分）:
|  标准 | 得分  |
|  :-:  | :-:  |
| 没有人会使用，没有实用性 | 0 |
| web2的产品迁移到web3而已 | 1 |
| 目前市场缺口，利用web3能解决目前存在的绝大多数问题  | 2|

- 新颖性（满分2分）:
|  标准 | 得分  |
|  :-: | :-:  |
| 比较陈旧的产品方向 | 0 |
| 比较有意思 | 1 |
| 有创意，让人眼前一亮 ，Aha | 2|

- 市场是否有同类产品（满分2分）:
|  标准 | 得分  |
|  :-: | :-: |
| 同类产品较多，已形成头部市场| 0 |
| 同类产品较少，无头部产品 | 1 |
| 无同类产品，蓝海市场  | 2|

### 5.技术栈评估（满分10分）
评分标准：统计团队成员的技术栈，所选取项目使用的技术栈和团队技术栈的匹配程度
- 技术栈Go、Javascript、Java
举例：如当前团队所使用的技术栈为Go、Javascript、Java，所选项目使用的技术栈为PHP, Javascript,Solidity,那么匹配度为 1/3，得分为 1/3x10= 3.33分

## 综合得分
根据各自团队的情况为上述细则中的每项取加权值，比如各项都为20%，那么一个项目的每项得分如下
|  维度 | 得分  |  加权值 |
|  :-:  | :-:  | :-:  |
| 代码功能完整性 | 9 |20%|
| 代码实现完整性 | 9 |20%|
| 项目质量 | 10 |20%|
| 产品性评估 | 8 |20%|
| 技术栈评估 | 6 |20%|

**总分为：**9x20% + 9x20% + 10x20% + 8x20% + 6x20% = 8.4分
**评估结果：可以进行迁移**
