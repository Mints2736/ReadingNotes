Chapter 7. Classes
=====

说到 Class， 就不得不提两个概念：**抽象(data abstraction)**和**封装(encapsulation)**。

何谓**抽象**？就是程序语言中一种**将接口(interface)与实现(implementation)相分离**的技术。何谓**封装**？就是对上述技术的一种具体实践。所以我们可以说，是封装实践了抽象。抽象是一种思想，封装是一种手段。

经过封装，我们可以定义出一种抽象的数据结构，用户不必关心其内部实现，只需要考虑用它做什么。从而抽身繁琐的细节实现中，将注意力集中在具体需求上。

-----

更深一步思考，抽象这个思想是怎么来的？这和人类的大脑结构有关，即使是聪明绝顶的人，也无法做到事无巨细的考虑某个复杂的问题。面对复杂的问题，我们首先想到的应该是如何将其细分，用术语来说，就是**分治法**。这是最核心的一种算法思想，我们都知道算法的定义，本质是一套步骤，第一步干什么，第二步干什么，一个清单一样的东西，而这些步骤，其实就是**分而治之**的一种体现。这与军事上讲的“各个击破”，政治上讲的“连横”都是一个道理。然而，能否真正的化简复杂问题，核心在于“如何细分”，即细分的依据。

一个普遍的常识是，分清**主次、轻重、缓急**，能够有效的处理复杂的事务。具体到计算机领域，对于一个丰富经验的程序员来说，具体实现就是次、轻、缓，而理解需求，并将需求转化为领域模型、层次架构、算法结构，才是主、重、急。在学校老师常常说，写具体代码的都是流水的兵，做设计与架构的才是核心人员。这也从侧面反映了上述的主次轻重与缓急之分。

那么，领域模型考虑的是什么？说白了就是贴近业务用例的语言。下过象棋的人都知道有一个横冲直闯的“车”，这个“车”，有哪些特点？可以用它做什么？这些就是领域模型规定的事情。如，我们可以写出：

车，属性：当前位置；操作：横移，纵移，顶替在移动过程中遇到障碍物的位置。

我们描述象棋里面“车”这个东西，就要像类似上面这样，说清楚它必须具备什么属性，可以进行什么必备的操作。到这个层次就可以了。根据这个信息，系统设计人员，就可以画出总体类图了。

属性，操作，这都是面向对象中的词汇。在Java/C++里，我们一般说数据，成员(data, member)和接口(interface)、方法(function)。可统称为 interface.

那么，属性用什么数据结构记录，操作采用什么方式实现，如何与其他的棋子交互(吃与被吃)，这些就是具体实现的范畴。可称为 implementation.

架构师的领域模型，直接对应着 interface 这一层，implementation 这一层却无法对应上，所以，分开他们很有必要。

综上所述，抽象是一种看全局、抓重点的思想；封装是对 interface 与 implementation 的一种分离。

-----
