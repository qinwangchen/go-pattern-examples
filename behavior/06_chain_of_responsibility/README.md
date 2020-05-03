# 职责链模式

职责链模式用于动态组合一些行为，在go实现相对更为简单，行为模式中提到的option模式跟此模式很像，但是两者场景用例不同，op模式的行为常常用于对象初始化或者某一过程中设置参数，职责链主要作用在于动态组合行为链，以便处理特定的对象或者问题。


中间件模式就是一个典型的职责链模式，一个对象，在中间件中层层传递，每一层都可以进行自己的处理。


Golang实现职责链模式时候，因为没有继承的支持，使用链对象包涵职责的方式，即：

* 链对象包含当前职责对象以及下一个职责链。
* 职责对象提供接口表示是否能处理对应请求。
* 职责对象提供处理函数处理相关职责。

同时可在职责链类中实现职责接口相关函数，使职责链对象可以当做一般职责对象是用。