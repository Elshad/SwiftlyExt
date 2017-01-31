![](Logo/logo.png)

[![Build Status](https://travis-ci.org/khoiln/SwiftlyExt.svg?branch=master)](https://travis-ci.org/khoiln/SwiftlyExt)
[![codecov](https://codecov.io/gh/khoiln/SwiftlyExt/branch/master/graph/badge.svg)](https://codecov.io/gh/khoiln/SwiftlyExt)
[![CocoaPods Compatible](https://img.shields.io/cocoapods/v/SwiftlyExt.svg)](https://img.shields.io/cocoapods/v/SwiftlyExt.svg)
[![Carthage Compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)
![Swift 3.0.x](https://img.shields.io/badge/Swift-3.0.x-orange.svg)
[![Platform](https://img.shields.io/cocoapods/p/SwiftlyExt.svg?style=flat)](http://cocoadocs.org/docsets/SwiftlyExt)
[![MIT](https://img.shields.io/badge/License-MIT-red.svg)](https://opensource.org/licenses/MIT)

SwiftlyExt is a library that extends certain Swift standard types and classes using extension feature in the Swift language.

- [Requirements](#requirements)
- [Installation](#installation)
- [Documentation via CocoaDocs](http://cocoadocs.org/docsets/SwiftlyExt/)
- [FAQ](#faq)
- [License](#license)

## Requirements

- iOS 9.0+ / macOS 10.11+ / tvOS 9.0+ / watchOS 2.0+
- Xcode 8.0+
- Swift 3.0+

## Installation

### CocoaPods

[CocoaPods](http://cocoapods.org) is a dependency manager for Cocoa projects. You can install it with the following command:

```bash
$ gem install cocoapods
```

> CocoaPods 1.1.0+ is required to build SwiftlyExt.

To integrate SwiftlyExt into your Xcode project using CocoaPods, specify it in your `Podfile`:

```ruby
source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '10.0'
use_frameworks!

target '<Your Target Name>' do
    pod 'SwiftlyExt', '~> 1.1'
end
```

Then, run the following command:

```bash
$ pod install
```

### Carthage

[Carthage](https://github.com/Carthage/Carthage) is a decentralized dependency manager that builds your dependencies and provides you with binary frameworks.

You can install Carthage with [Homebrew](http://brew.sh/) using the following command:

```bash
$ brew update
$ brew install carthage
```

To integrate SwiftlyExt into your Xcode project using Carthage, specify it in your `Cartfile`:

```ogdl
github "khoiln/SwiftlyExt" ~> 1.1
```

Run `carthage update` to build the framework and drag the built `SwiftlyExt.framework` into your Xcode project. U

### Swift Package Manager

Adding SwiftlyExt as a dependency is as easy as adding it to the `dependencies` value of your `Package.swift` file.

```swift
dependencies: [
    .Package(url: "https://github.com/khoiln/SwiftlyExt.git", majorVersion: 1)
]
```

Note that the [Swift Package Manager](https://swift.org/package-manager/) is still in early design and development, but SwiftlyExt does support its use on supported platforms.

## Usage

There are many handy usages of `SwiftlyExt`, head over [CocoaDocs](http://cocoadocs.org/docsets/SwiftlyExt/) for the comprehensive documentation.

We'll try to list some of the cool examples here.

### Array Extensions

```swift
// Return a random element
[😀,🤡,❤️,💋].sample() // => 💋
// Return n random elements
[😀,🤡,❤️,💋].sampleSize(2) // => [🤡, 💋]
//Check if all elements in the array passed the condition
[0, 11, 28, 10].every { $0 % 2 == 0 } // => false
//Check if one of the element passes the condition
[0, 11, 28, 10].some { $0 % 2 != 0 } // => true
//Find index of the last number which predicate return true for.
[1, 2, 3, 4, 5].findLastIndex {$0 % 2 == 0} // => 3 
//Group common elements from an array to a dictionary of [Hashable : [Element]]
[1, 2, 3, 4, 5].groupBy { $0 % 2 == 0 ? "even" : "odd"} // => ["even": [2,4], "odd": [1,3,5]]
```

## How to contribute
Any help or feedback is highly appreciated. Please refer to the [contributing guidelines](https://github.com/khoiln/SwiftlyExt/blob/master/CONTRIBUTING.md) for more information.

## License

SwiftyExt is released under the MIT license. See [LICENSE](https://github.com/khoiln/SwiftlyExt/blob/master/LICENSE) for details.
