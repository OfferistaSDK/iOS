# iOS Offerista brochure widget SDK

## Installation
CocoaPods

[CocoaPods](https://cocoapods.org/) is a dependency manager for Cocoa projects. For usage and installation instructions, visit their website. To integrate OfferistaBrochureWidget SDK into your Xcode project using CocoaPods, specify it in your ```Podfile```:

```
use_frameworks!
pod 'OfferistaBrochureWidget', '7.0.0'
```

Add the below configuration to your Podfile-

```
post_install do |installer|
  installer.pods_project.targets.each do |target|
    if target.name == 'PromiseKit'
      target.build_configurations.each do |config|
        config.build_settings['BUILD_LIBRARY_FOR_DISTRIBUTION'] = 'YES'
      end
    end
  end
end
```
