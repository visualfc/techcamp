# 从类型系统理解 iXGo 解释器的实现

编程语言的类型系统可以分为编译时类型系统（程序编译阶段进行静态类型检查的机制）和运行时类型系统（程序执行期间动态管理类型信息的机制）。
从类型系统角度来看，XGo 兼容 Go 编译时类型系统，LLGo 兼容 C 运行时类型系统，iXGo 兼容 Go 运行时类型系统。

- 七叶 GitHub 个人主页：[https://github.com/visualfc](https://github.com/visualfc)

iXGo 解释器兼容 Go 语言运行时类型系统，支持 Go 语言全部特性。通过使用 `xgobuild` 扩展包，也可以将 XGo 语言编译为 Go 语言并解释执行。

本文重点关注的是 iXGo 解释器，从运行时类型系统角度来理解 iXGo 解释器的实现。

### iXGo 解释器执行流程

[https://github.com/goplus/ixgo](https://github.com/goplus/ixgo)
