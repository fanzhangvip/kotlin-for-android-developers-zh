# 集合和函数操作符

在我们这个项目我们已经使用过集合了，但是现在是时候展示它们结合函数操作符之后有多强大了。关于函数式编程很不错的一点是我们不用去解释我们怎么去做，而是直接说我想做什么。比如，如果我想去过滤一个list，不用去创建一个list，遍历这个list的每一项，然后如果满足一定的条件则放到一个新的集合中，而是直接食用filer函数并指明我想用的过滤器。用这种方式，我们可以节省大量的代码。

虽然我们可以直接用Java中的集合，但是Kotlin也提供了一些你希望用的本地的接口：

- __Iterable__：父类。所有我们可以遍历一系列的都是实现这个接口。
- MutableIterable：一个支持便利的同时可以执行删除的Iterables。
- __Collection__：这个类相是一个范性集合。我们通过函数访问可以返回集合的size、是否为空、是否包含一个或者一些item。这个集合的所有方法提供查询，因为connections是不可修改的。
- __MutableCollection__：一个支持增加和删除item的Collection。它提供了额外的函数，比如`add` 、`remove`、`clear`等等。
- __List__：可能是最流行的集合类型。它是一个范性有序的集合。因为它的有序，我们可以使用`get`函数通过position来访问。
- __MutableList__：一个支持增加和删除item的List。
- __Set__：一个无序并不支持重复item的集合。
- __MutableSet__：一个支持增加和删除item的Set。
- __Map__：一个key-value对的collection。key在map中是唯一的，也就是说不能有两对key是一样的键值对存在于一个map中。
- __MutableMap__：一个支持增加和删除item的map。

有很多不同集合的可用的函数操作符。我想通过一个例子来展示给你看。知道有哪些可选的操作符是很有用的，因为这样会更容易分辨它们使用的时机。