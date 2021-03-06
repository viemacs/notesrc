---
title: Norm
weight: 20
---

## Code Review

#### 为什么做 Code Review
做 Code review 是为了改进代码质量. 通过对代码, 测试过程和注释进行检查, 来确认方案设计和代码实现.

Code review 的主要目的:

1. 保证代码质量

- 程序逻辑
- 需求和设计的实现
- 查找和排除系统缺陷
- 可读性
- 可维护性

- 保证项目组人员的良好沟通 
- 项目或产品的代码更容易维护 

2. 提高参与者开发水平
- 传递作者的意图和想法，使其他人可以更加熟悉代码，利于维护代码和改进代码
- 评审过程使大家更多的理解系统，重构思路，
- 确定作者的设计和实现清晰，简单
- 帮助初级开发人员学习高级开发人员的经验，达到知识共享, 相互学习，提高开发者水平

次要目的:
- 查找程序的bug
- 保证代码风格和编码标准
- 编码风格
- 避免开发人员犯一些很常见，很普通的错误 
- 在项目早期就能够发现代码中的BUG 

消除 Bug 主要靠测试. 由单元测试，功能测试，性能测试，回归测试来消除Bug。
单元测试为主。单元测试最接近bug，bug没有扩散的地方。
在 code review 之前，要有单元测试和单元测试报告，

代码风格和编码标准是确定的, 是靠个人可以做到的, 所以在代码提交时就应该是符合规范的。
代码规范，有作者自己和一些检查代码规范的工具。

规范性
- 注释格式
- 命名规范

- 异常处理
- 日志处理
- 代码组织结构

- 业务实现

在开发过程中, 对源代码进行系统检查.
查找代码缺陷,
检查功能实现,
编码合理性,
性能优化.

整理思路，流程的实现方法， 代码的组织方法（不是风格）

#### CR 的过程
完整的 Code Review 包括三个阶段: 准备, 执行, 追踪

1. 准备
    1. 代码  
	   控制所要 review 的代码数量. 如果代码量比较大, 可对代码按功能模块进行分解,
	   确定(各部分的)关键代码, 对关键代码进行 review
	2. review 的重点
	3. 规范  
	   review 的规范用于交流时的统一, 有标准可遁, 提高 review 沟通的效率效果
	4. 确定参与者  
	   把 review 的代码, 重点, 规范和流程发给所有参与者
    5. 执行方式
	   git 式, meeting 式, 1对1 / 多对1 式
2. implement 执行  
    1. 准确记录  
	   对于CR过程发现的问题，我们必须清晰准确的记录，可以使用问题点记录单，明确记录的项目和内容。
	2. 讲解与提问
	   CR过程中，要采用代码作者讲解和审查者提问方式。审查者不能只在发现问题时提问，同时也要根据本次审查的内容要求代码作者对某个特定问题的讲解。
	3. 逐项审查  
	   对事前确定的审查内容，要逐项审查，不能因为时间不足等因素一扫而过。
3. 追踪
    1. 确认问题信息
	   - 问题的影响范围, 解决的难易程度
	   - 解决问题的时限
	   - 由谁来解决, 由谁来确认
    2. 解决过程记录
	   - 问题的原因
	   - 解决对策
	   - 修改的内容
	3. 确认结果  
	   按时限对修改结果进行全面确认


#### 说明

1. 经常做 Code Review, 保持较短的 review 间隔
    - 一个人写代码的时间长了, 会在代码中加入越来越多的个性化的东西 :p
	- 一次 review 的代码越多, 要修改重构的也越多, 会在讨论中产生太多口水
	- 问题解决得越靠前, 总体上所要做的修改就越少
2. Code Review 要快速, 不要拘泥形式
    - 严格按形式进行 Code Review 的问题:
	    - 只有在 checklist 上的项目才会被 review
		- reviewer 在形式上花的精力多了, 在实际思考代码上的精力和耐心就会少
    - 可以花5分钟, 给人讲一下你的代码, 然后花5分钟, 听听他对你代码的意见和想法
	
	- 觉得有用处的地方, 再做成材料
	- 要能放松, 再放松, 把真正想说的说出来
	
2.0. code review 的过程是讨论问题, 解决问题  
	记住Review只不过是一种形式，而只有在相互信任中通过相互的讨论得到了有意义和有建设性的建议和意见，那才是最实在的。不然，作者和评审者的关系就会变成小偷和警察的关系。

3. 每人都需要让不同的人 review 你的代码  
   - 每次可以找两三个人来做 review, 这样3,4个人可以围在一起讨论, 每个人都能充分参与, 也不会因为意见太多降低执行的效率
   - 不同的人有不同的思考方式, 对同一功能和设计的实现有不同的想法, 可以从不同方向更全面地来过你的代码
   - 参与的人可以更好地理解你的代码, 团队中每个人的思考可以更同步, 在日后代码维护时相互帮助也更容易

4. Enjoy 学会享受  
   傲慢是程序员三大美德之一. 当看别人的代码时, 或者代码被人修改时, 自负的情绪会让人不容易接受不同的想法.
   Code review 需要一种积极的态度提意见和接受意见, 不要抨击别人的代码, 不要质疑别人的能力, 
   给同事的建议和同事给的建议, 都是为了大家能做得更好.  
   Code review 的核心是讨论问题, 解决问题. 
   团队里人人都喜欢讨论问题, 解决问题, 那每个人都能写高质量的代码, 
   大家相互学习, 相互帮助, 每个人都能更好地进化, 团队能快速适应变化.  
   关键是, 开心的才是更好的 :-)


#### 准备工作

1. 参与人对自己在 code review 要做什么, 要学什么有基本的了解
2. 代码能正确运行/编译, 功能基本正确
3. 代码能通过单元测试和测试用例
4. 做 review 的人对代码有基本的了解,
   代码的功能是什么, 涉及什么系统的什么方面, 对性能,稳定等方面有什么特别的需求,
   好有针对性地检查代码

Code review 前代码的语法和功能问题应该已经解决, review 的重点在代码质量上.


#### GIT 提交

1. 提交日志有明确的含义，明确此次提交的内容或目的
像“修改了某文件”，“更行了某文件”提供的信息太少。

写日志时考虑log的目的是在查找修改bug，版本回滚，代码评审等过程中提供有效的信息。

2. 提交的大小
提交的代码太多，不便于代码评审和版本控制.
提交太多太小的修改，会影响版本和日志的可读性。
可以参考的做法是，对一个模块完成修改，昨晚单元测试后，压缩commit之后提交。

避免的做法：提交未测试的代码，出现问题后提交很多小的修改。


#### Review 项目
基本方面
- 代码一致性
- 代码安全问题
- 代码冗余
- 设计的正确性
- 性能与功能需求

代码中使用的格式、符号、结构等风格是否保持一致 

1. 完整性 completeness
    1. 完全实现设计文档中的功能需求
	2. 创建并初始化了所需要的数据库
	3. 去除了未定义或未使用的变量, 常量, 类
2. 一致性 consistency
    1. 代码逻辑与文档中逻辑是否一致
	2. 代码中的算法符合文档中的数学模型
3. 正确性 correctness
	1. 注释准确完整
	2. 函数调用参数传递正确
	3. 变量定义和使用方式正确
    4. 代码组织方式符合制定的标准
4. 清晰性 clearness
    1. 所需的数据字典, 接口说明, 描述如何访问常量, 变量, 功能
    2. 配置, 定义文件是否易于理解, 修改
	3. 功能模块功能的入口和出口明确, 唯一
	4. 函数的出口唯一 (异常处理除外)
    5. 每个功能都是一个可辩识的代码块
5. 可预测性 predictability
    1. 代码语言中常见陷阱已检测并排除
	2. 是否有依赖于开发工具环境语言缺省提供的功能
	3. 代码中没有死循环, 无穷递归
6. 健壮性 robustness
    - 采取措施避免运行时错误: 数组边界溢出, 被零除, 值越界, 堆栈溢出, etc
7. 可追溯性 traceability
    1. 每个程序有唯一标识
	2. 代码和开发文档之间有交叉引用(框架)可以相互对应
	3. 代码版本管理中对代码的修改和原因都有易于理解的记录
8. 可读性 readability
    1. 注释清晰描述了每个子程序
	2. 复杂代码有必要的使用理由, 注释清楚明确
	3. 使用一些统一的格式化技巧（如缩进、空白等）用来增强代码的清晰度
	4. 变量, 函数的命名清楚反映含义, 便于记忆, 书写
	5. 变量都有合理合法的取值范围
9. 可验证性 verifiability
    - 代码中功能的实现方式便于测试

#### Review 步骤
1. 作者向参与review的人按用例或功能依次讲解自己的代码功能, 相关逻辑
2. reviewer 提出疑问, 组织者对存在的问题做记录
3. reviewer 自己对代码进行审核, 并把问题和修改建议记录在表中
4. 组织者把各reviewer的代码问题记录表汇总成"review报告", 记录发现的问题和修改建议，然后把"review报告"发送给相关人员
5. 作者根据"review报告"的修改意见修改代码, 有不清楚的地方和reviewer进行交流
6. 作者在过完 issue 之后作出反馈
7. 组织者把 Code Review 中发现的有价值的问题更新到 "code review 规范" 文档中
8. 对值得提醒和注意的问题可 email 给所有技术人员

#### 所需文档
- code review 规范
- issue 记录表
- issue 汇总表
- issue 解决表
- meeting 记录
- output to protocol documents

#### ref

相关资料
[5个开源的代码审查工具] (http://coolshell.cn/articles/1218.html)

资料来源

- [Code Reivew的执行] (http://www.cnblogs.com/dinofung/articles/2302957.html)
- [Code Review中的几个提示] (http://coolshell.cn/articles/1302.html)
- [什么是Code Review] (http://www.cnblogs.com/wdpp/archive/2011/01/17/2386823.html)
- [web项目经理手册-Code Review] (http://blog.csdn.net/yzhz/article/details/1669802)
