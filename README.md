# Swifty - Make swift code swifty

中文 | [English](README-EN.md)

[![CI Status](https://img.shields.io/travis/RyukieSama/RyukieSwifty.svg?style=flat)](https://travis-ci.org/RyukieSama/RyukieSwifty)
[![Version](https://img.shields.io/cocoapods/v/RyukieSwifty.svg?style=flat)](https://cocoapods.org/pods/RyukieSwifty)
[![License](https://img.shields.io/cocoapods/l/RyukieSwifty.svg?style=flat)](https://cocoapods.org/pods/RyukieSwifty)
[![Platform](https://img.shields.io/cocoapods/p/Swifty.svg?style=flat)](https://cocoapods.org/pods/RyukieSwifty)

## 一、 示例程序

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## 二、 CocoaPods 完整安装

```ruby
pod 'RyukieSwifty'
```

## 三、 按功能安装

### 3.1 UIKit Extension

```ruby
pod 'RyukieSwifty/UIKit'
```

### 3.2 CloudKit Extension

```ruby
pod 'RyukieSwifty/CloudKit'
```

### 3.3 Foundation Extension

```ruby
pod 'RyukieSwifty/Foundation'
```

### 3.4 全屏控制

```ruby
pod 'RyukieSwifty/FullScreen'
```

### 3.5 路由协议

```ruby
pod 'RyukieSwifty/Router'
```

### 3.6 网络请求接口协议 - MoyaStyleProtocol

通过该协议可以使 `Swift` 内容中的网络请求实现有 `Moya` 的风格，更加 `Swifty`，不依赖具体第三方网络库，易于切换拓展。

```ruby
pod 'RyukieSwifty/SwiftyServiceProtocol'
```

### 3.7 截屏防护 (>= iOS13)

极其轻量化的截屏防护方案，任何需要被保护的 `View` 作为子视图放入 `ScreenShieldView` 即可达到截屏时隐藏内容的效果。

![ScreenShield](ScreenShield.gif)

```ruby
pod 'RyukieSwifty/ScreenShield'
```

Swift - Demo: 

```Swift
import UIKit
import RyukieSwifty

class ViewController: UIViewController {
    override func loadView() {
        view = ScreenShieldView.create()
    }
    ...
}
```

OC - Demo:

```C++
#import "OCScreenShieldViewController.h"
@import RyukieSwifty;

@interface OCScreenShieldViewController ()

@end

@implementation OCScreenShieldViewController

- (void)loadView {
    self.view = [ScreenShieldView createWithFrame:UIScreen.mainScreen.bounds];
}

- (void)viewDidLoad {
    [super viewDidLoad];
    
    UIView *cubeView = [[UIView alloc] initWithFrame:CGRectMake(100, 100, 100, 100)];
    cubeView.backgroundColor = [UIColor redColor];
    [self.view addSubview:cubeView];
    
    self.view.backgroundColor = [UIColor grayColor];
}

@end
```

## 四、 作者

RyukieSama, ryukie.sama@gmail.com

## License

Swifty is available under the MIT license. See the LICENSE file for more info.


