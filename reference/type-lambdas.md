# 类型lambda

类型 lambda 在不额外定义的类型的情况下，产生一个高阶类型。

```scala
[+X, Y] => Map[Y, X]
```

例如上面就定义了一个包含一个协变类型参数 `X` 和一个不可变类型参数 `Y` 的二元类型构造器。这个类型构造器能将类型 `S` 和 `T` 映射到类型 `Map[T, S]`。类型 lambda 的类型参数能够具有变异性以及边界指定。一个这样的参数化类型类型定义

```scala
type T[X] = (X, X)
```

是一个定义右侧是一个类型 lambda 的简单类型定义的简写：

```scala
type T = [X] => (X, X)
```

