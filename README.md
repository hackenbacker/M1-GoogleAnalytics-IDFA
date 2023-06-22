# Description
I met the following error when building an App with GoogleAnalytics and GoogleIDFASupport on M1 mac.
```
🔴 In (...)/Pods/GooglelDFASupport/Libraries/libAdldAccessLibrary.a(TAGActualAddAccess.o),
building for iOS Simulator, 
but linking in object file built for iOS, 
file '(...)/Pods/GooglelDFASupport/Libraries/libAdIdAccessLibrary.a' 
for architecture arm64
🔴 Linker command failed with exit code 1 (use -v to see invocation)
```

 I solved the problem by changing the version of `GoogleIDFASupport` to `3.12.0`. (see `Podfile`)

 This repository is the minimum configuration for GoogleAnalytics and GoogleIDFASupport to be built on Apple Silicon machines.


# How to setup
```sh
pod install
```

# Development Environment
## OS
* iOS 13.0 - 17.0 beta

## Xcode
* Xcode 14.3.1
* Xcode 15.0 Beta

## CocoaPods
* 1.11.2, 1.12.1

## Mac
* M1 Ultra
* M1 Pro
* Bitrise - M1 Medium (Xcode 14.1)
