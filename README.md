# CBZSplashView

[![CI Status](http://img.shields.io/travis/Callum Boddy/CBZSplashView.svg?style=flat)](https://travis-ci.org/Callum Boddy/CBZSplashView)
[![Version](https://img.shields.io/cocoapods/v/CBZSplashView.svg?style=flat)](http://cocoadocs.org/docsets/CBZSplashView)
[![License](https://img.shields.io/cocoapods/l/CBZSplashView.svg?style=flat)](http://cocoadocs.org/docsets/CBZSplashView)
[![Platform](https://img.shields.io/cocoapods/p/CBZSplashView.svg?style=flat)](http://cocoadocs.org/docsets/CBZSplashView)


## CBZSplashView

Inspired by the Twitter Splash screen.

Create a splash view no disimilar to the one Twitter use.

just drop in your logo and choose a background color and you are ready to go.

I have also added some customization options if you are that way inclined.

Twitter: 
(I seldom say anything, but when I do you propably want to here it.)
<a href="https://twitter.com/callumboddy">@callumboddy</a> 

<img src="Images/twitterGif.gif"/>

Easy as pie:
```objective-c
  UIImage *icon = [UIImage imageNamed:kMyIcon];
  UIColor *color = [UIColor colorWithHexString:kMyColor];
  CBZSplashView *splashView = [[CBZSplashView alloc] initWithIcon:icon backgroundColor:color];
  
  // customize duration, icon size, or icon color here;
  
  [self.view addSubview:splashView];
  [splashView startAnimation];
```
  
or you can animate on completion if you want to..
```objective-c

  [self downloadLoadsOfAmazingContentWithCompletion:^(BOOL success, NSError *error) {
    [splashView startAnimation];
  }];
```

## Usage

To run the example project, clone the repo, and run.

## Installation

CBZSplashView is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

    pod "CBZSplashView"

## Updates

0.1.1:
- feature: added propery to manipulate the icon size, eg. splashView.iconStartSize = CGSizeMake(200, 200);
- feature: added propery to manipulate the icon color, eg. splashView.iconColor = [UIColor redColor];
- feature: added propery to manipulate the animation Duration, eg. splashView.animationDuration = 2; (in seconds)

- change: animtion no longer fires automatically, you must call [splashView startAnimation];

0.1.0 - done on the train, very messy


## Author

Callum Boddy, callum.boddy@gmail.com

## License

CBZSplashView is available under the MIT license. See the LICENSE file for more info.

