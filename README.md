# PXDToolkit

[![CI Status](http://img.shields.io/travis/pixeldock/PXDToolkit.svg?style=flat)](https://travis-ci.org/pixeldock/PXDToolkit)
[![Version](https://img.shields.io/cocoapods/v/PXDToolkit.svg?style=flat)](http://cocoapods.org/pods/PXDToolkit)
[![License](https://img.shields.io/cocoapods/l/PXDToolkit.svg?style=flat)](http://cocoapods.org/pods/PXDToolkit)
[![Platform](https://img.shields.io/cocoapods/p/PXDToolkit.svg?style=flat)](http://cocoapods.org/pods/PXDToolkit)
[![Swift](https://img.shields.io/badge/Swift-3.x-orange.svg?style=flat)](https://swift.org/)
[![Twitter](https://img.shields.io/badge/Twitter-@pixeldock-blue.svg?style=flat)](http://twitter.com/pixeldock)

## Requirements
iOS 8.0 or Greater  
Swift 3.1

If you are using Swift 2.3 use PXDToolkit version 0.2.1

## Installation

PXDToolkit is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "PXDToolkit", '~> 0.3'
```
If you are using Swift 2.3 use PXDToolkit version 0.2.1:
```ruby
pod "PXDToolkit", '0.2.1'
```

Add this to your podfile (if it is not already there) to make the pod work with Swift 3.1 (or Swift 2.3):

```swift
post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['SWIFT_VERSION'] = '3.1' # or '2.3'
    end
  end
end
```

## Usage

<h4>Int</h4>
**Random Int between 0 and 10**
```swift
let randomInt = 10.random
```
----------
<h4>Array</h4>
**Get random element from Array**
```swift
let randomElement = ["A", "B", "C"].randomElement
```
**Get 2 random elements from Array**
```swift
let randomElements = ["A", "B", "C"].randomElements(2)
```
**Shuffle array (order elements randomly)**
```swift
let shuffledArray = ["A", "B", "C"].shuffled
```
----------
<h4>UIColor</h4>
**Color from hex int value**
```swift
let darkRedColor = UIColor(hex: 0xAA0000)
```
**Color from hex int value with alpha**
```swift
let darkRedColor = UIColor(hex: 0xAA0000, alpha: 0.5)
```
**Hex string from Color**
```swift
let redColorHexString = UIColor.redColor().hexString
```
----------
<h4>CGFloat</h4>
**Degrees to Radians**
```swift
let angleRadians = CGFloat(180).degreesToRadians
```
**Radians to Degrees**
```swift
let degrees = CGFloat(3.1415).radiansToDegrees
```
----------
<h4>NSLocalizedString</h4>
If your *Localizable.strings* file contains this:
```
"GREETING" = "Hello";
"TEMPERATURE" = "It is %f.01°C in %@";
```
You can do this:
**Get localized string for a key**
```swift
print(LocalizedString("GREETING")) // "Hello"
```
And this:
**Get localized string with dynamic parts**
```swift
print(LocalizedString("TEMPERATURE", arguments:[21.8, "Paris"])) // "It is 21.8°C in Paris"
```
----------
<h4>UIApplication</h4>
**Get App version**
```swift
let appVersion = UIApplication.appVersion()
```
**Get Build number**
```swift
let buildNumber = UIApplication.appBuild()
```
----------
<h4>Timing Functions</h4>
**Delay**

Delays the execution of the closure. Always runs on the main thread.
```swift
delay(seconds: 2) {
   print("hello!")
}
```

## Author

Jörn Schoppe, joern@pixeldock.com

Comments and suggestions are highly welcome!

## License

PXDToolkit is available under the MIT license. See the LICENSE file for more info.
