+++
date = '2025-08-07T13:15:19+08:00'
draft = false
title = 'C++之旅'
+++

## 项目构建

采用[CMake](https://cmake.org/cmake/help/latest/guide/tutorial/index.html)自动化构建项目，不想看官方文档可以参看以下两篇文章：

1. [CMake 保姆级教程（上）](https://subingwen.cn/cmake/CMake-primer/index.html#1-CMake%E6%A6%82%E8%BF%B0)
2. [CMake 保姆级教程（下）](https://subingwen.cn/cmake/CMake-advanced/)

---

## 测试

代码的测试一般采用[GoogleTest](https://google.github.io/googletest/samples.html)，注意其和CMake的集成，在`FetchContent_Declare`时获取最新的版本。

---

## 序列化/反序列化

经常会需要将数据序列化然后放到网络上传输并从网络上接收数据反序列化回来，此时可以利用[nlohmann/json](https://github.com/nlohmann/json)这个库帮助我们序列化/反序列化数据。通过该库提供的`NLOHMANN_DEFINE_TYPE_NON_INTRUSIVE`等宏可以超级轻松地实现数据的序列化和反序列化。
