# iOS 开发调试工具

[![CI Status](https://img.shields.io/travis/icofans/TTConsole.svg?style=flat)](https://travis-ci.org/icofans/TTConsole)
[![Version](https://img.shields.io/cocoapods/v/TTConsole.svg?style=flat)](https://cocoapods.org/pods/TTConsole)
[![License](https://img.shields.io/cocoapods/l/TTConsole.svg?style=flat)](https://cocoapods.org/pods/TTConsole)
[![Platform](https://img.shields.io/cocoapods/p/TTConsole.svg?style=flat)](https://cocoapods.org/pods/TTConsole)

## 环境切换

方便在开发调试期间切换环境，切换后需重启生效，启动时直接在Appdelegate读取 [[TTConsole console].currentEnvironment] 当前环境，然后对项目环境进行切换配置

## 网络请求

拦截App内网络请求，可详细查看请求的具体内容，方便调试过程中监测

## 调试日志

在App内查看调试产生的日志信息

## 崩溃收集

对崩溃进行收集查看

## 沙盒浏览

浏览沙盒文件

## 安装

```ruby
pod 'TTConsole'
```
# 使用

在 - (void)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions 方法注册

```objc
#if DEBUG
    [[TTConsole console] enableDebugMode];
    NSLog(@"[当前启动环境为%@]",@[@"内网测试", @"外网测试", @"外网生产"][[TTConsole console].currentEnvironment]);
#endif
```
