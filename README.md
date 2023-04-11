# TensorFlowLiteSwift

Swift package of TensorFlowLiteSwift

Downloaded binary frameworks from official CocoaPods and repackaged for Swift package manager

## Swift package manager

```
.package(url: "https://github.com/tensorflow/tensorflow/tree/master/tensorflow/lite", .branch("master"))
```

## Add TensorFlow Lite to your Swift or Objective-C project

TensorFlow Lite offers native iOS libraries written in Swift. Start writing your own iOS code using the Swift gesture classification example as a starting point. The sections below demonstrate how to add TensorFlow Lite Swift or Objective-C to your project:

### CocoaPods developers
In your Podfile, add the TensorFlow Lite pod. Then, run pod install.

### Swift
```
use_frameworks!
pod 'TensorFlowLiteSwift'
```

### Specifying versions
There are stable releases, and nightly releases available for both TensorFlowLiteSwift. If you do not specify a version constraint as in the above examples, CocoaPods will pull the latest stable release by default.

You can also specify a version constraint. For example, if you wish to depend on version 2.10.0, you can write the dependency as:

```
pod 'TensorFlowLiteSwift', '~> 2.10.0'
```

This will ensure the latest available 2.x.y version of the TensorFlowLiteSwift pod is used in your app. Alternatively, if you want to depend on the nightly builds, you can write:

```
pod 'TensorFlowLiteSwift', '~> 0.0.1-nightly'
```

From 2.4.0 version and latest nightly releases, by default GPU and Core ML delegates are excluded from the pod to reduce the binary size. You can include them by specifying subspec:

```
pod 'TensorFlowLiteSwift', '~> 0.0.1-nightly', :subspecs => ['CoreML', 'Metal']
```

This will allow you to use the latest features added to TensorFlow Lite. Note that once the Podfile.lock file is created when you run pod install command for the first time, the nightly library version will be locked at the current date's version. If you wish to update the nightly library to the newer one, you should run pod update command.

