# What Is 软件建模？
  
软件设计中最重要的概念就是抽象，如果没有多变的需求，也许就没有今天的面向对象软件。

## [多变且复杂的需求](https://www.jdon.com/mda/modeling.html)

我们曾经试图通过需求管理、需求跟踪等等管理方式约束和减少需求频繁更新带给软件的冲击，这样下去的结果只有一个：
使得软件更加僵化；  
或者程序员更加劳累。

需求不但多变，而且经常是不可能第一次就能掌握，每个特定案例需求又有其特别复杂之处，
几乎没有人能够第一次接触就可以深入掌握这些专业领域的需求本质，就是专门的建模专家也不例外
需求反映了某个领域的专业知识，例如数学、管理、财务或 电子商务等等。

既然需求是多变而且复杂的，所以，就不能使用“堵”式方法对其进行控制和管理，
只能顺势而为，通过灵活多变的 以及迭代反复的方式逐步抓住需求。
并且作为需求的实现软件系统必须能够迅速应对需求变化，需求变化有多快，软件变化就有多快。

引入灵活多变的架构，面向对象 OO 架构正是应对多变需求而生，
强调软件的可维护性和扩展性，OO 可能不是最好方式，但是目前是最合适的。

对于复杂的需求，我们的解决之道是，委派专门的建模专家跟踪理解需求，在需求和需求实现之间搭建桥梁。
项目方法上采取多次迭代的敏捷软件开发方式，逐步了解学习掌握需求。

## 需求分析方法演变

### 第一阶段：围绕数据库的驱动的分析设计

新软件项目总是从设计数据库及其字段开始，这个阶段特征就是围绕数据库编程。
典型的是 DBase/Foxpro，以及后来的Delphi/VB技术。

* 缺点

首先，不能迅速有效全面认识反映需求，世界不只是由简单的关系数据组成，
而且使用关系数据来反映现实需求，不符合人类自然思维（OO才是）是一种扭曲的分析方法。

在运行性能方面，容易导致软件运行时负载集中在数据库端，
系统性能难于扩展（走上集中式、昂贵的、高风险的大型机模式）。
闲置了中间件J2EE服务器分布式集群处理能力，就是使用了集群，也分担不了负载。

对象和关系数据库存在阻抗，本身是矛盾竞争的，他们是两种分析看待需求的流派，可以说是水火不容。
要么你采取数据库分析设计以及过程化编程，要么完全采取OO。
现在使用.NET和Java这样OO语言的人很多，但是70%左右都是使用OO语言，
编写传统过程化系统，在Java中这样做，会有极差性能。

### 第二阶段：面向对象的分析设计方法诞生后

有了专门的分析和设计阶段之分，我们使用UML符号来表达分析设计思想，
分析设计进入了一个相对更高的层次，拥有了自己一套科学且艺术的方法论。

* 缺点

分析阶段和设计阶段是断裂的，互相不能很好衔接

*** 为什么? ***

分析人员的职责是负责从需求领域中收集基本概念，
设计人员的职责必须指明一组能被项目中适应编程工具构造的组件，
这些组件必须能够在目标环境中有效执行，并能够正确解决应用程序出现的问题 两个阶段两者目标不一致。

分析人员只管需求分析，至于是否适合设计，或者能够导出适宜设计的分析结果，这个尺度很难衡量和把握。
而设计人员因为照顾代码可运行，因此，经常可能会抱怨分析员给出的结果过于粗糙，
不适合设计，这样分析设计两个阶段就导致分裂，项目失败。

* UML

在这个阶段，虽然有UML帮助，但是UML不是思想。

### 第三阶段 融合了分析阶段和设计阶段的领域驱动设计

领域建模是一种艺术的技术，抛弃了分裂分析模型与设计的做法，使用单一的模型来满足这两方面的要求，这就是领域模型。
单一的领域模型同时满足分析原型和软件设计，如果一个模型实现时不实用，重新寻找新模型。
