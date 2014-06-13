/*********bruce0505(大熊)************/

#Swift常见问题解答

Swift 是Apple发布的一种全新的、现代化的、类型安全的编程语言，它针对Cocoa开发。Swift已经被研发了4年之久，在今年刚刚过去的WWDC大会上发布。

Swift采用了许多语言中很受欢迎的结构特点，这些语言包括Objective-C, Rust, Haskell, Ruby, Python, C#, CLU等等。

可以去看看泰然论坛最近发表的关于[Swift语言亮点](http://www.tairan.com/archives/6624)的文章，那里有详细的描述。

Swift的语言更加简单和简洁，降低了iOS开发的门槛，而且让开发过程更舒服。

在这篇关于Swift的FAQ中，我们将解答很多提问频率很高的问题，这些问题我们经常在论坛、Twitter、邮件和StackOverflow网站上看到。按照这个模式我们也将定期的在这篇FAQ中更新一些新问题。

注意这里面有些答案只是一些意见或者推测，因此对它们要持怀疑态度。我们很欢迎看到你自己的一些想法或者意见，并且基于你的反馈我们将对应的来更新这个FAQ。

##基础知识

###我是一个初学者，我应该学Objective-C，还是Swift，或者两者都学？

在我们看来，这取决于你打算做一个独立开发者，还是去另一家iOS公司去工作。

- **如果你打算去一个iOS公司做全职开发或者顾问**：两者都学习是最好的，这是因为很多iOS公司都有基于Objective-C的已有代码，这些都需要你去了解和学习，而且有些公司不会马上就过渡到Swift。你需要去弄明白大量用Objective-C写的iOS库、教程和例子代码。长远来看你需要去学习Swift并且慢慢过渡到Swift。

- **如果你是一个独立开发者**：如果一开始你只打算用Swift，从理论上讲你只要了解Swift就可以。但是如果你能抽出一些时间，深入理解一下Objective-C是非常好的，这样你就能使用现有Objective-C资源中包含的大量的API库。

多年后随着前景的发展和Swift接受度的增长，这些答案可能会改变。最后，知道Objective-C可能就类似于知道COBOL(可能意味Objective-C会像COBOL一样变成一门古老的语言)。

###我已经做了多年的Objective-C开发。我现在要重新开始学么？

是和不是，如果你一直在Apple平台发展，你仍然有着巨大的优势，因为你已经熟悉了Xcode和Cocoa/Cocoa Touch相关的API。跟学习Swift相比，学习Xcode和数量庞大的Cocoa/Cocoa Touch 相关API要耗费更多的时间，因此你应该在处于比较良好的状态。

长话短说，一旦你写Swift代码熟练了，你回感觉到很舒适自在—而且对于你来说，应该会很快的就学会Swift。

###iOS和OS X Yosemite应用程序会只使用Swift开发么？

不会，Apple已经将Swift进行了构造，让Swift可以和Objective-C流利的进行互操作，反之亦然！对于Objective-C的API和框架，Apple还未完全将其转换成Swift，但是仍然可以在你自己的Swift代码中使用。

这些只有时间来证明，但是在Swift慢慢被采纳的过程中，可能许多iOS和OS X应用商店还会持续的依赖Objective-C很多年。

###Swift可以在其它版本的iOS和OS X下运行么？


是的！Xcode 6可以编译Swift代码并在iOS 7及以上或者OS X 10.9及以上部署生成目标。Apple其实已经用Swift开发了一个WWDC app，你现在就可以从App Store下载试用！

不过要记住Apple不允许从Xcode的测试版本构建的app发布到App Store。因此你需要等到Xcode 6的最终版本发布之后，再将你用Swift写得app提交到App Store。

###Swift是要取代Objective-C，还是对Objective-C的补充？


引述Apple的话，“Objective-C不会消失，Swift和Objective-C两者都是做Cocoa和Cocoa Touch开发的最好工具”。

所以你可以继续使用Objective-C。然而Apple似乎在鼓励用Swift来开发新的应用，而不希望你回去将你之前的Objective-C代码重新写一遍。

然而这完全是推测，大家都在猜测在将来的框架和API开发中，Apple会逐渐减少Objective-C的使用，甚至有一天Objective-C可能会被废弃。因此，赶紧跳上Swift的火车加入raywenderlich.com的团队来吧:)

###什么是playground？

playground是一个你可以进行实时代码效果预览的文件，这对于学习Swift或者新的API，编写原型代码或者开发算法是非常棒的功能。

当你要说你将要去playground的时候小心你的孩子。就像Chris LaPollo所学到的，由于你没带孩子们去公园，当你坐到电脑前的时候，孩子们可能会在你身后大哭！

###开发者保密协议(NDA)解除了么？

现在还不清楚这方面的情况。最近iOS开发者协议条款中有了这样的更新：

**
此外，关于Apple在WWDC(Apple全球开发者大会)预发布的Apple软件和服务的技术信息，Apple同意您不会受上述保密条款约束，但是您不可以屏幕截图，写公众评论或者重新发布任何预发布版的Apple软件或服务。
**

另外，Apple公开发布了一本[Swift编程](https://itunes.apple.com/us/book/swift-programming-language/id881256329?mt=11&uo=8&at=11ld4k&uo=8&at=11ld4k&uo=8&at=11ld4k)的书，而且iOS 8 的SDK文档也是公开的。在往年，这样的信息直到新版本的iOS发布之后才会被公开。

就编写教程来说还不清楚这意味着什么。现在有种影响力较大/较流行的说法是[只要不提交截图](http://oleb.net/blog/2014/06/apple-lifted-beta-nda/)你就可以写教程。但这也不是很确定，就像[Chris Adamson指出的](http://www.subfurther.com/blog/2014/06/04/dub-dub-disclosure-conference/)。

在我们看来，由于Swift编程教程是公开的，看上去Swift语言本身是公平的游戏，但是对于Xcode 6的截图或者Chris提出的其它一些问题我们还不确定，这些对于编写教程来说都是很必要的。

我们正试着从Apple得到一些解释，然后弄清楚这些，如果/当我们查清楚我们会更新这个帖子。

###怎样学Swift？

这里已经有学习Swift的一些非常好的资源：

- Apple的[Swift编程](https://itunes.apple.com/us/book/swift-programming-language/id881256329?mt=11&uo=8&at=11ld4k&uo=8&at=11ld4k&uo=8&at=11ld4k)

- 你也可以像Xcode中playground那样边实践边读这些书(Help\Documentation and API Reference\New Features in Xcode 6 Beta\Swift Language\The Swift Programming Language\A Swift Tour\Open Playground)

- [WWDC2014](https://developer.apple.com/videos/wwdc/2014/)大会的Swift视频

- Swift[速查和参考](http://www.raywenderlich.com/73967/swift-cheat-sheet-and-quick-reference)或许会有助于你向Swift的过渡

很快我们也会发布大量的额外资源 – 有关这方面请查看下一个问题！

###你们将来的书或者教程是否会使用Swift？

简短回答—是的！我们正尽最大力帮助大家过渡到Swift。

详细回答：

- **iOS8教程(iOS 8 by Tutorials)**:这本书会用Swift来写，帮助大家过渡到这种新语言。我们也将为那些还没准备好过渡到Swift的小伙伴提供Objective-C写的示例项目，以帮助他们对比两种语言。

- **iOS游戏教程(iOS Games by Tutorials)**:我们也将更新iOS游戏教程(Swift开发) — 同时我们还将很快宣布另一个激动人心的更新/变化。

- **书面教程(Written tutorials)**:一旦开发者保密协议(NDA)解除了，我们将会在未来的书面教程中使用Swift。我们也将会把我们许多老的书面教程更新为Swift。后面将详细讨论。

- **视频教程(Video tutorials)**:很快我们将会发布很多关于Swift/iOS 8的视频教程，并且将我们的许多视频教程更新为Swift！

- **一些惊喜…**:我们还有一些惊喜来吸引你 – 敬请关注!:)

/***********NickYang(街坊)*************/
##Diving Right In
译：马上行动
###Is there anything that Swift can do that Objective-C can’t, and vice-versa?
译：Swift是否能做一些Objective-C做不了的事情，又或者Objective-C能做的Swift做不了？

Yes! Swift is a modern language that introduces many things that Objective-C does not support. Some of the big things include namespacing, optionals, tuples, generics, type inference and many more.

译：答案是肯定的！Swift是一门提供了许多Objective-C并不支持的特性的现代语言。其中一些大的特性包括命名空间(namespacing), 可选择（optionals）, 元组（tuples），泛型（generic），类型推导（type inference）等。

Objective-C also has some “features” that are not available in Swift like messaging nil.

译：Objective-C也拥有一些特性是Swift并不支持的，例如给一个nil值发送消息(messaging nil).

It would be in your best interest to read the [Using Swift with Cocoa and Objective-C Guide](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/BuildingCocoaApps/index.html#//apple_ref/doc/uid/TP40014216-CH2-XID_0) by Apple for more details – after reading this post of course!

译：在看完这帖子之后，读者如果有兴趣获取更多细节的话可以阅读由苹果公司提供的指南：[Using Swift with Cocoa and Objective-C Guide](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/BuildingCocoaApps/index.html#//apple_ref/doc/uid/TP40014216-CH2-XID_0)
###Are there any APIs that don’t work with Swift?

译：是否有些库接口（APIs）是Swift不支持的？

At the time of writing this post, I am not aware of any. There are however some caveats on how to move things between Objective-C and Swift APIs. Here are some examples:
译：在写这个帖子的时候，我还没有发现有不支持的。 但是，在Objective-C和Swift的接口之间进行移植的时候需要注意一些问题，例如：

- When an Objective-C API returns an `id`, Swift will receive `AnyObject`.

译： 当一个Objective-C接口返回一个‘id’类型的时候，Swift收到的将是‘AnyObject’类型。


- When an Objective-C API returns `nil`, Swift will receive an `Optional` set to the value `NONE` which is Swift’s way of saying a variable is `nil`. Because Swift variables must always contain a value, it uses the `Optional` enum for any object returned from an Objective-C API being that there is no guarantee that an Objective-C method won’t return `nil`.

译：当Objective-C接口返回‘nil’时，Swift返回的值将是一个值为‘None’的‘Optional’（这是Swift表示一个变量是nil的方式）。因为Swift变量必须总是有值，由于不能保证一个Objective-C方法不返回nil值，所以它使用了‘Optional’枚举所有从一个Objective-C接口返回的对象。

- When an Objective-C API returns a collection it will be typed to `AnyObject` due to the inability to infer what type an `NSArray` or `NSDictionary` stores. It is a good practice to downcast your collections when they are returned based on what you know of the API. Consider an Objective-C method that returns an array of `NSString `instances. Because you know that the returned array contains strings, you can safely downcast in the following manner.

译：当一个Objective-C接口返回一个容器的时候，Swift将会返回‘AnyObject’，只是由于它无法推导出一个‘NSArray’或者‘NSDictionary’存放的是什么类型的数据。 当被返回的容器是基于你所知道的接口，一个很好的方式就是把容器类型向下类型转换。想想一个Objective-C方法返回一个NSString实例数组。因为你知道返回的数组包含的是一些字符串，所以你可以很安全的使用以下方式进行向下类型转换。


```
let fruits : AnyObject[] = // some Objective-C API that returns NSArray of NSStrings
 
for fruit in fruits as String[] {
    println(fruit)
}
```

- When a Swift API returns a Tuple, Objective-C will receive… nothing! Since tuples are not supported in Objective-C, the method won’t be available to Objective-C code. There are a number of Swift constructs that Objective-C cannot support. These include…

译：当一个Swift接口返回一个元组的时候，Objective-C将不会接收到任何东西。因为元组在Objective-C中是不被支持的，在Objective-C代码中元组相关的方法是无法被利用的。下面有一些是Objective-C不支持的Swift结构：

	- Generics
	译：泛型
	- Tuples
	译：元组
	- Enumerations defined in Swift
	译：定义在Swift的枚举类型
	- Structures defined in Swift
	译：定义在Swift的结构体
	- Top-level functions defined in Swift
	译：定义在Swift的顶层函数
	- Global variables defined in Swift
	译：定义在Swift的全局变量
	- Typealiases defined in Swift
	译：定义在Swift的类型别名
	- Swift-style variadics
	译：Swift风格的可变参数
	- Nested types
	译：嵌套的类型
	- Curried functions
	译：柯里化函数
	
###Where are my println() results in my Playground?
译：println()结果显示在PlayGround的什么地方？

You must turn on the Assistant Editor to see your console output. Do this via **View > Assistant Editor > Show Assistant Editor** or by the keystroke **Option + Command + Return**.

译：为了能看到控制台的输出，你必须打开Assistant Editor。 你可以通过选择**View > Assistant Editor > Show Assistant Editor** 或者按 **Option + Command + Return**键来打开Assistant Editor。

Thanks to [Chris LaPollo](http://www.raywenderlich.com/u/clapollo) for providing insight on this one!

译：感谢[Chris LaPollo](http://www.raywenderlich.com/u/clapollo) 提供了关于这方面的信息
###How do I see those cool graphs of values in Playgrounds?
译：在Playgrounds如何查看那些很酷的值图

You can graph the results of values over time in Playgrounds, which can be really handy for visualizing algorithms.

To do this, enter some code that produces values over time like this in a playground:

译：你可以在Playgrounds上图形化显示一个值在不同时间的结果，这对算法的可视化十分便利。你可以在PlayGround里面通过输入一些代码实现在不同时间产生一些值，譬如：

```
for x in 1..10 {
  x
}
```

In the sidebar, you’ll see something like “9 times”. Move your mouse over this line, and a + button will appear. Click this button (and make sure your Assistant Editor is open) and you should see the graph.

译：在边栏上，你可以看到一些内容，例如“9 times”。 把鼠标移动到这一行上面，将会有一个“+”按钮出现。点击这个按钮（保证你的Assistant Editor是打开的），然后你就可以看到这个图了

###How do you run the REPL?

译：如何运行REPL(Read-Eval-Print-Loop: 读验证打印循环)？

Run the following command in Terminal to tell it to use Xcode 6′s command line tools.

译：在终端上执行以下命令来让使用Xcode 6的命令行工具

```
sudo xcode-select -s /Applications/Xcode6-Beta.app/Contents/Developer/
```

Then run the following to start the Swift REPL.

译：然后执行下面的命令来开启Swift REPL

```
xcrun swift
```

When you are ready to exit you can type `:exit` or `:quit`. You can also use the **CTRL+D** keystroke.

译：当你想退出REPL的时候你可以输入 `:exit` 或者 `:quit`来退出。你也可以使用快捷键 **CTRL+D** 

###Can you use Swift to call your own Objective-C code or a third party library? If so, how?

译：你能使用Swift来调用你自己的Objective-C代码或者第三方库么？如果可以，该怎么实现？

Yes! When you add your first .swift file to your Xcode Project you will be prompted to let Xcode create a bridging header file. In that header file you can import the Objective-C headers that you want to be visible to your Swift code.

译：可以的！当你添加你的第一个.swift文件到你的Xcode工程的时候你将收到让Xcode创建一个桥接头文件的提示。在那个头文件里面你可以导入要被你的Swift代码访问的Objective-C头文件。

Then, all of those classes will be available to your Swift code without further imports. You can use your custom Objective-C code with the same Swift syntax you use with system classes.

译：接着，你不必再进行import，就可以在你的Swift代码使用这些类。你可以用Swift调用系统类同样的语法来使用你的自定义Objective-C代码。


###So, arrays can only contain one type of object? What if I want varied types?

译：那么数组只能包含一种对象类型？那如果我想要包含多个对象类型，该怎么做？

In Swift you are highly encouraged to make strongly typed arrays that contain only one type of object, with syntax like this:

译：在Swift中，鼓励开发者使用只包含一种对象类型的强类型数组，语句可以想这样：
```
var goodArray: String[] = ["foo", "bar"]
```

That said, technically you can still create arrays that contain multiple types of objects. However, before you do this you should be asking yourself `why` you want to do this. In most cases it does not make the best sense and you can likely engineer your solution to be cleaner.

译：那就是说，从技术上你仍可以创建包含多个对象类型的数组。然而，在你这样做的时候你应该问问自己“为什么”你要这样做。在大多数情况下这种方式并不是最好的，或许你可以设计更加简洁的方案来代替。

With that said, here’s how you can create a Swift array with varying types of objects within it by using `AnyObject`:

译：按照这种说法，下面告诉你使用‘AnyObject’创建一个具有不同对象类型的Swift数组:

```
var brokenArray: AnyObject[] = ["foo", 1, 12.23, true]
```

###Is the same true for dictionaries? Are dictionaries also strongly typed?

译：对于字典类型（dictionaries）是否也是这样？字典类型是否也应该是强类型？
Yes, but again you can get around this by using `AnyObject`. For dictionaries it often might make sense that not all of the values in your dictionary are of the same type. Consider a JSON response from a server that is represented as a dictionary:

译：是的！但是同样你可以使用‘AnyObject’来避免它。对于字典类型，它常常可能并不是所有的值都是同一种类型。想想由服务端发送过来的一个以字典类型表现的Json格式的响应：

```
var employee : Dictionary<String, AnyObject> = ["FirstName" : "Larry", "LastName" : "Rodgers", "Salary" : 65_000.00]
```

This dictionary contains two keys with `String` values and one key with a `Double` value. Although this is achievable, you should opt to create first class model objects to represent your data rather than relying on Dictionaries when possible.

译：这个字典包含了两个‘String’类型的键值和一个‘Double’类型的键值。虽然这种方式实现没有问题，但是你应该选择创建第一类模型对象（first classs model objects）来表示你的数据，而尽量不依赖字典。

/***************evachen1984(数羊)******************/
##The Nitty Gritty

###Is there an equivalent to id in Swift?

Yes. As mentioned above when an Objective-C API returns `id` Swift will substitute with `AnyObject`. The `AnyObject` type can represent an instance of any class type. There is also `Any` which can represent an instance of any type at all (apart from function types).

###How do you do introspection in Swift? (e.g. equivalent of if ([obj isKindOfClass:[Foo class]]) { … })?

You can check the type of a variable or constant using the `is` keyword. The compiler is smart enough to let you know if using `is` would be redundant. Thanks to type safety in Swift, it is not possible to later assign a different type to the same reference, which makes this possible.

```
var someValue : AnyObject?
 
someValue = "String"
 
if someValue is String {
    println("someValue is a String")
} else {
    println("someValue is something else")
}
```

Notice if you try to write…

```
var someValue = "String"
 
if someValue is String {
    println("someValue is a String")
} else {
    println("someValue is something else")
}
```

You will receive a compiler warning:

```
Playground execution failed: error: <REPL>:7:14: error: 'is' test is always true
if someValue is String {
```

###How do you put bitshifted values inside an enum in Swift? (i.e. MyVal = 1<<5)

Unfortunately this is a bit confusing and definitely **not** as succinct as the C variant. Rather than using an `enum` you will be using a `struct` as shown below.

```
struct MyOptions : RawOptionSet {
    var value: UInt = 0
    init(_ value: UInt) { self.value = value }
    func toRaw() -> UInt { return self.value }
    func getLogicValue() -> Bool { return self.value != 0 }
    static func fromRaw(raw: UInt) -> MyOptions? { return MyOptions(raw) }
    static func fromMask(raw: UInt) -> MyOptions { return MyOptions(raw) }
 
    static var None: MyOptions          { return MyOptions(0) }
    static var FirstOption: MyOptions   { return MyOptions(1 << 0) }
    static var SecondOption: MyOptions  { return MyOptions(1 << 1) }
    static var ThirdOption: MyOptions   { return MyOptions(1 << 2) }
}
 
func == (lhs: MyOptions, rhs: MyOptions) -> Bool     { return lhs.value == rhs.value }
func | (lhs: MyOptions, rhs: MyOptions) -> MyOptions { return MyOptions(lhs.value | rhs.value) }
func & (lhs: MyOptions, rhs: MyOptions) -> MyOptions { return MyOptions(lhs.value & rhs.value) }
func ^ (lhs: MyOptions, rhs: MyOptions) -> MyOptions { return MyOptions(lhs.value ^ rhs.value) }
```

Credit goes to [Nate Cook](http://stackoverflow.com/users/59541/nate-cook) for this one, check out [his answer on Stack Overflow](http://stackoverflow.com/a/24066171) with more details.

###How does Swift work with Grand Central Dispatch?

The same way, you can use the C APIs as you did in Objective-C.

```
dispatch_async(dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_BACKGROUND, 0), {
    println("test")
});
```

You can also use the higher level `NSOperationQueue` as prescribed by Apple when dealing with concurrency.

###What about the internationalization macros from Objective-C?

Similar to the NSLocalizedString set of macros from Objective-C you can prepare for internationalization in Swift code by using the **NSLocalizedString(key:tableName:bundle:value:comment:)** method. The `tableName`, `bundle`, and `value` arguments all have default values. So if you’re used to using `NSLocalizedString` you can write the following.

```
NSLocalizedString("Hello", comment: "standard greeting")
```

###Do I need to worry about reference cycles?

Absolutely! It is still possible to create a retain cycle when two objects have a `strong` reference to each other. To break retain cycles you would use a similar approach that you use in Objective-C. There are three keywords for declaring reference types which are described below; `weak` and `unowned` will allow you to resolve reference cycles.

###When should I use strong vs. weak vs. unowned references?

- **strong**: You should use `strong` for things you own.
Strong references cause ARC to retain instances until they are no longer needed. When all `strong` references are removed the referenced instance is deallocated.

	Note that the `strong` reference is implied by default, so you do not explicitly declare it.

- **weak**: You should use `weak` for references among objects with independent lifetimes.
	
	When you set a `weak` reference to an object, you’re saying that it’s OK with you if the object is deallocated due to memory pressure. Weak values must always be a variable, defined with `var` and must also be Optional using the `?` operator.

	Since weak references are optional, you will never end up with a reference to an invalid instance that no longer exists. ARC will automatically set the reference to nil when the referenced instance is deallocated.

- **unowned**: You should use unowned for objects with the same lifetime; such as when an object points back to its owner and you wish to avoid a retain cycle.
The `unowned` reference is used whenever a reference will always have a value but when you need to tell ARC to not set the reference to nil.

	`unowned` behaves similarly to `unsafe_unretained` in Objective-C. You are responsible for ensuring that you do not access the reference after the referenced object is deallocated, doing so will result in your app crashing. Unowned references must **not** be optional and cannot be set to `nil`. Unowned references are also implicitly unwrapped.
	
###Where are the semi-colons?!

Semi-colons are optional in Swift and Apple suggests you stop using them for readability purposes.

However, sometimes semicolons are still used in Swift, such as in for statements:

```
for var index = 0; index < 3; ++index { ... }
```
/***********紫夜行者***************/
##What’s Next?
译:下一步是什么？
###What is the future of Swift?
译:Swift下一步有何打算？

This is only version 1, Apple’s intentions are [clear](https://twitter.com/clattner_llvm/status/474774351024107520) that they will be iterating on this language.
译:当前是版本1，对于这门语言苹果的意图遍历他们是明确简洁的。

So be sure to [report bugs and request features](http://bugreport.apple.com/)! There is a lot of room to see improvements before version 1 is officially released.
译：所以一定要报告错误信息并请求特征。在正式版本1发布我们看到有很多地方得到改进。

###How will CocoaPods adapt to swift?
译：CocoaPods响应swift速度如何？

Likely in a similar way. Swift projects still work as Xcode projects and support multiple targets. There is however potential room for improvement with the ability to create modules and custom frameworks.
译：几乎一样的使用方法。Swift项目仍然使用xcode开发并且支持多个targets。在自定义模块和框架时它还有很多潜在提高的地方。

It is possible that CocoaPods will be reworked to utilize this feature. There are people who have CocoaPods [working with Swift projects](https://medium.com/swift-programming/cocoapods-with-swift-e6f8ba8f0afc) and the smart people who work on CocoaPods are already [discussing this topic](https://github.com/CocoaPods/CocoaPods/issues/2218).

译:为了使用此特性CocosPods被重写是可行的。用CocoaPods与Swift项目工作的人和少部分使用CocoaPods工作的人已经讨论这个问题了。

##More Questions?
译:更多问题？

If you have any questions that were not covered here (I know you do!) please post a comment. I will pick out some of the best ones and update the post with the question and answer – and also give you attribution for asking!

译：如果你有任何问题请提交你们疑问。我会挑选一些好的问题并更新问题和回复。-- 和给你回馈！

Also, as mentioned earlier, please chime in with any comments or clarifications on the answers listed here and I’ll update as appropriate.

译:另外，正如前面提到的，请在这里列出的你的答案或者任何意见或澄清，我会及时更新。

Thanks all, and happy Swift’ing!

译:非常感谢大家，并祝大家使用Swift愉快！^_^