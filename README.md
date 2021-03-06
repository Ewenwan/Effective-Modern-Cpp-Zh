Effective Modern C++
====================

42 SPECIFIC WAYS TO IMPROVE YOUR USE OF C++11 AND C++14

Effective Modern C++ 中文翻译，欢迎大家提出翻译中的错误和用词不当的地方。

[《Effective Modern C++》翻译 - 2018.5更新中 其他](https://github.com/Ewenwan/EffectiveModernCppChinese)

![Effective Modern C++](book.jpg)


## 代码使用说明

使用gitbook作为静态编译输出，需要安装`Node.js`，然后从`npm`安装gitbook

```sh
npm install gitbook -g
```

然后git clone下来本书，然后输出静态网页，在浏览器上查看：

```sh
git clone git@github.com:XimingCheng/Effective-Modern-Cpp-Zh.git
cd Effective-Modern-Cpp-Zh
gitbook serve .
```

gitbook会默认在端口`4000`开启服务器，使用浏览器访问[http://localhost:4000/](http://localhost:4000/)就可以访问然后阅读本书的中文翻译。随后我会将本书编译生成的静态网页上传至github pages。

* [出版者的忠告](FromthePublisher/README.md)
* [致谢](Acknowledgements/README.md)
* [简介](Introduction/README.md)
* [第一章 类型推导](DeducingTypes/README.md)
 - [条款1：理解模板类型推导](DeducingTypes/1-Understand-template-type-deduction.md)
 - [条款2：理解auto类型推导](DeducingTypes/2-Understand-auto-type-deduction.md)
 - [条款3：理解decltype](DeducingTypes/3-Understand-decltype.md)
 - [条款4：知道如何查看类型推导](DeducingTypes/4-Know-how-to-view-deduced-types.md)
* [第二章 auto关键字](auto/README.md)
 - [条款5：优先使用auto而非显式类型声明](auto/5-Prefer-auto-to-explicit-type-declarations.md)
 - [条款6：当auto推导出非预期类型时应当使用显式的类型初始化](auto/6-Use-the-explicitly-typed-initializer-idiom-when-auto-deduces-undesired-types.md)
* [第三章 使用现代C++](MovingtoModernC++/README.md)
 - [条款7：创建对象时区分()和{}](MovingtoModernC++/7-Distinguish-between-xxx-when-creating-objects.md)
 - [条款8：优先使用nullptr而不是0或者NULL](MovingtoModernC++/8-Prefer-nullptr-to-0-and-NULL.md)
 - [条款9：优先使用声明别名而不是typedef](MovingtoModernC++/9-Prefer-alias-declarations-to-typedefs.md)
 - [条款10：优先使用作用域限制的enmu而不是无作用域的enum](MovingtoModernC++/10-Prefer-scoped-enum-to-unscoped-enums.md)
 - [条款11：优先使用delete关键字删除函数而不是private却又不实现的函数](MovingtoModernC++/11-Prefer-deleted-functions-to-private-undefined-ones.md)
 - [条款12：使用override关键字声明覆盖的函数](MovingtoModernC++/12-Declare-overriding-functions-override.md)
 - [条款13：优先使用const_iterator而不是iterator](MovingtoModernC++/13-Prefer-const_iterators-to-iterators.md)
 - [条款14：使用noexcept修饰不想抛出异常的函数](MovingtoModernC++/14-Declare-functions-noexcept-if-they-won’t-emit-exceptions.md)
 - [条款15：尽可能的使用constexpr](MovingtoModernC++/15-Use-constexpr-whenever-possible.md)
 - [条款16：保证const成员函数线程安全](MovingtoModernC++/16-Make-const-member-functions-thread-safe.md)
 - [条款17：理解特殊成员函数的生成](MovingtoModernC++/17-Understand-special-member-function-generation.md)
* [第四章 智能指针](SmartPointers/README.md)
 - [条款18：使用std::unique_ptr管理独占资源](SmartPointers/18-Use-std-unique_ptr-for-exclusive-ownership-resource-management.md)
 - [条款19：使用std::shared_ptr管理共享资源](SmartPointers/19-Use-std-shared_ptr-for-shared-ownership-resource-management.md)
 - [条款20：在std::shared_ptr类似指针可以悬挂时使用std::weak_ptr](SmartPointers/20-Use-std-weak_ptr-for-std-shared_ptr-like-pointers-that-can-dangle.md)
 - [条款21：优先使用std::make_unique和std::make_shared而不是直接使用new](SmartPointers/21-Prefer-std-make_unique-and-std-make_shared-to-direct-use-of-new.md)
 - [条款22：当使用Pimpl的时候在实现文件中定义特殊的成员函数](SmartPointers/22-When-using-the-Pimpl-Idiom-define-special-member-functions-in-the-implementation-file.md)
* [第五章 右值引用、移动语义和完美转发](RvalueReferencesMoveSemanticsandPerfectForwarding/README.md)
 - [条款23：理解std::move和std::forward](RvalueReferencesMoveSemanticsandPerfectForwarding/23-Understand-std-move-and-std-forward.md)
 - [条款24：区分通用引用和右值引用](RvalueReferencesMoveSemanticsandPerfectForwarding/24-Distinguish-universal-references-from-rvalue-references.md)
 - [条款25：在右值引用上使用std::move 在通用引用上使用std::forward](RvalueReferencesMoveSemanticsandPerfectForwarding/25-Use-std-move-on-rvalue-references-std-forward-on-universal-references.md)
 - [条款26：避免在通用引用上重定义函数](RvalueReferencesMoveSemanticsandPerfectForwarding/26-Avoid-overloading-on-universal-references.md)
 - [条款27：熟悉通用引用上重定义函数的其他选择](RvalueReferencesMoveSemanticsandPerfectForwarding/27-Familiarize-yourself-with-alternatives-to-overloading-on-universal-references.md)
 - [条款28：理解引用折叠](RvalueReferencesMoveSemanticsandPerfectForwarding/28-Understand-reference-collapsing.md)
 - [条款29：假定移动操作不存在，不廉价，不使用](RvalueReferencesMoveSemanticsandPerfectForwarding/29-Assume-that-move-operations-are-not-present-not-cheap-and-not-used.md)
 - [条款30：熟悉完美转发和失败的情况](RvalueReferencesMoveSemanticsandPerfectForwarding/30-Familiarize-yourself-with-perfect-forwarding-failure-cases.md)
* [第六章 Lambda表达式](LambdaExpressions/README.md)
 - [条款31：避免默认的参数捕捉](LambdaExpressions/31-Avoid-default-capture-modes.md)
 - [条款32：使用init捕捉来移动对象到闭包](LambdaExpressions/32-Use-init-capture-to-move-objects-into-closures.md)
 - [条款33：在auto&&参数上使用decltype当std::forward auto&&参数](LambdaExpressions/33-Use-decltype-on-auto&&-parameters-to-std-forward-them.md)
 - [条款34：优先使用lambda而不是std::bind](LambdaExpressions/34-Prefer-lambdas-to-std-bind.md)
* [第七章 并发API](TheConcurrencyAPI/README.md)
 - [条款35：优先使用task-based而不是thread-based](TheConcurrencyAPI/35-Prefer-task-based-programming-to-thread-based.md)
 - [条款36：当异步是必要的时声明std::launch::async](TheConcurrencyAPI/36-Specify-std-launch-async-if-asynchronicity-is-essential.md)
 - [条款37：使得std::thread在所有的路径下无法join](TheConcurrencyAPI/37-Make-std-threads-unjoinable-on-all-paths.md)
 - [条款38：注意线程句柄析构的行为](TheConcurrencyAPI/38-Be-aware-of-varying-thread-handle-destructor-behavior.md)
 - [条款39：考虑在一次性事件通信上void的特性](TheConcurrencyAPI/39-Consider-void-futures-for-one-shot-event-communication.md)
 - [条款40：在并发时使用std::atomic 在特殊内存上使用volatile](TheConcurrencyAPI/40-Use-std-atomic-for-concurrency-volatile-for-special-memory.md)
* [第八章 改进](Tweaks/README.md)
 - [条款41：考虑对拷贝参数按值传递移动廉价，那就尽量拷贝](Tweaks/41-Consider-pass-by-value-for-copyable-parameters-that-are-cheap-to-move-and-always-copied.md)
 - [条款42：考虑使用emplace代替insert](Tweaks/42-Consider-emplacement-instead-of-insertion.md)
