# 工厂方法模式

工厂方法模式使用子类的方式延迟生成对象到子类中实现。

不同的工厂对象，返回一个实现了某接口的类型对象，不同的工厂返回不同实现了相同接口的不同对象，在只能使用特定的类简单工厂的基础上，使用的代码和类生成的灵活性大大增加。

Go中的继承关系是使用匿名组合来实现的。
