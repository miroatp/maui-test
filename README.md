### ATPWTAJointApp

Simple .NET 8.0 MAUI app based on the official template to test the Plugin.Firebase.* packages.

Expected: The app builds on both platforms
Actual: The app does not build for iOS simulator. The terminal log:
```
 *  Executing task: dotnet build -t:Build -p:Configuration=Debug -f net8.0-ios -r iossimulator-arm64 -p:CustomAfterMicrosoftCSharpTargets="/Users/miroslavkouril/.vscode/extensions/ms-dotnettools.dotnet-maui-1.0.6-darwin-arm64/dist/resources/Custom.After.Microsoft.CSharp.targets" -p:MauiVSCodeBuildOutputFile="/var/folders/5l/39_hr8w90nx1d4ys4qjzg52h0000gp/T/dotnet-maui/maui-vsc-ca5842d3-6956-4c70-a9d2-a0282f254ae8.json" -p:XamlTools="/Users/miroslavkouril/.vscode/extensions/ms-dotnettools.csharp-2.34.10-darwin-arm64/.xamlTools" /Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj 

MSBuild version 17.9.8+b34f75857 for .NET
  Determining projects to restore...
  Restored /Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj (in 605 ms).
  Detected signing identity:
          
    Bundle Id: com.atptour.test
    App Id: com.atptour.test
  Including assemblies for Hot Reload support
  ATPWTAJointApp -> /Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/bin/Debug/net8.0-ios/iossimulator-arm64/ATPWTAJointApp.dll
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/tools/msbuild/iOS/Xamarin.Shared.targets(146,3): warning : The directory '/Users/miroslavkouril/Library/Caches/XamarinBuildDownload/GAppM-10.24.0/GoogleAppMeasurement-10.24.0/Frameworks' does not exist. [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
  Optimizing assemblies for size may change the behavior of the app. Be sure to test after publishing. See: https://aka.ms/dotnet-illink
  Optimizing assemblies for size. This process might take a while.
/Users/miroslavkouril/Library/Caches/XamarinBuildDownload/FAnlytcs-10.24.0/FirebaseAnalytics-10.24.0/Frameworks/FirebaseAnalytics.xcframework/ios-arm64_x86_64-simulator/FirebaseAnalytics.framework/FirebaseAnalytics : warning MT7091: The framework /Users/miroslavkouril/Library/Caches/XamarinBuildDownload/FAnlytcs-10.24.0/FirebaseAnalytics-10.24.0/Frameworks/FirebaseAnalytics.xcframework/ios-arm64_x86_64-simulator/FirebaseAnalytics.framework is a framework of static libraries, and will not be copied to the app. [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
  Tool xcrun execution finished (exit code = 1).
          
  ld: warning: Could not find or use auto-linked framework 'GoogleAppMeasurement'
  Undefined symbols for architecture arm64:
    "_APMAnalyticsConfiguration", referenced from:
        +[FIRAnalytics startWithConfiguration:options:] in FirebaseAnalytics(FIRAnalytics.o)
    "_APMAppMeasurementOriginFirebase", referenced from:
        +[FIRAnalytics startWithConfiguration:options:] in FirebaseAnalytics(FIRAnalytics.o)
    "_APMConsentSettings3P", referenced from:
        +[FIRAnalytics setConsent:] in FirebaseAnalytics(FIRAnalytics.o)
    "_APMFormattedEventName", referenced from:
        +[FIRAnalytics logEventWithOrigin:name:parameters:] in FirebaseAnalytics(FIRAnalytics.o)
    "_APMFormattedUserPropertyName", referenced from:
        +[FIRAnalytics setUserPropertyString:forName:] in FirebaseAnalytics(FIRAnalytics.o)
    "_APMIsAnalyticsCollectionDeactivated", referenced from:
        +[FIRAnalytics startWithConfiguration:options:] in FirebaseAnalytics(FIRAnalytics.o)
    "_APMIsAnalyticsCollectionEnabled", referenced from:
        +[FIRAnalytics startWithConfiguration:options:] in FirebaseAnalytics(FIRAnalytics.o)
    "_APMMonitorLogTagOptionKey", referenced from:
        +[FIRAnalytics startWithConfiguration:options:] in FirebaseAnalytics(FIRAnalytics.o)
    "_APMUserDataFieldEmailAddress", referenced from:
        +[FIRAnalytics initiateOnDeviceConversionMeasurementWithEmailAddress:] in FirebaseAnalytics(FIRAnalytics.o)
    "_APMUserDataFieldHashedEmailAddress", referenced from:
        +[FIRAnalytics initiateOnDeviceConversionMeasurementWithHashedEmailAddress:] in FirebaseAnalytics(FIRAnalytics.o)
    "_APMUserDataFieldHashedPhoneNumber", referenced from:
        +[FIRAnalytics initiateOnDeviceConversionMeasurementWithHashedPhoneNumber:] in FirebaseAnalytics(FIRAnalytics.o)
    "_APMUserDataFieldPhoneNumber", referenced from:
        +[FIRAnalytics initiateOnDeviceConversionMeasurementWithPhoneNumber:] in FirebaseAnalytics(FIRAnalytics.o)
    "_OBJC_CLASS_$_APMAdExposureReporter", referenced from:
        _OBJC_CLASS_$_FIRAAdExposureReporter in FirebaseAnalytics(FIRAAdExposureReporter.o)
    "_OBJC_CLASS_$_APMAnalytics", referenced from:
        objc-class-ref in FirebaseAnalytics(FIRAnalytics.o)
    "_OBJC_CLASS_$_APMConditionalUserProperty", referenced from:
        _OBJC_CLASS_$_FIRAConditionalUserProperty in FirebaseAnalytics(FIRAConditionalUserProperty.o)
    "_OBJC_CLASS_$_APMConditionalUserPropertyController", referenced from:
        _OBJC_CLASS_$_FIRAConditionalUserPropertyController in FirebaseAnalytics(FIRAConditionalUserPropertyController.o)
    "_OBJC_CLASS_$_APMEvent", referenced from:
        _OBJC_CLASS_$_FIRAEvent in FirebaseAnalytics(FIRAEvent.o)
    "_OBJC_CLASS_$_APMIdentifiers", referenced from:
        _OBJC_CLASS_$_FIRAIdentifiers in FirebaseAnalytics(FIRAIdentifiers.o)
    "_OBJC_CLASS_$_APMIdentity", referenced from:
        objc-class-ref in FirebaseAnalytics(FIRAnalytics.o)
    "_OBJC_CLASS_$_APMMeasurement", referenced from:
        objc-class-ref in FirebaseAnalytics(FIRAnalytics.o)
        objc-class-ref in FirebaseAnalytics(FIRAMeasurement.o)
        _OBJC_CLASS_$_FIRAMeasurement in FirebaseAnalytics(FIRAMeasurement.o)
    "_OBJC_CLASS_$_APMScreenViewReporter", referenced from:
        objc-class-ref in FirebaseAnalytics(FIRAScreenViewReporter.o)
        _OBJC_CLASS_$_FIRAScreenViewReporter in FirebaseAnalytics(FIRAScreenViewReporter.o)
    "_OBJC_CLASS_$_APMUserAttribute", referenced from:
        _OBJC_CLASS_$_FIRAUserAttribute in FirebaseAnalytics(FIRAUserAttribute.o)
    "_OBJC_CLASS_$_APMValue", referenced from:
        _OBJC_CLASS_$_FIRAValue in FirebaseAnalytics(FIRAValue.o)
    "_OBJC_METACLASS_$_APMAdExposureReporter", referenced from:
        _OBJC_METACLASS_$_FIRAAdExposureReporter in FirebaseAnalytics(FIRAAdExposureReporter.o)
    "_OBJC_METACLASS_$_APMConditionalUserProperty", referenced from:
        _OBJC_METACLASS_$_FIRAConditionalUserProperty in FirebaseAnalytics(FIRAConditionalUserProperty.o)
    "_OBJC_METACLASS_$_APMConditionalUserPropertyController", referenced from:
        _OBJC_METACLASS_$_FIRAConditionalUserPropertyController in FirebaseAnalytics(FIRAConditionalUserPropertyController.o)
    "_OBJC_METACLASS_$_APMEvent", referenced from:
        _OBJC_METACLASS_$_FIRAEvent in FirebaseAnalytics(FIRAEvent.o)
    "_OBJC_METACLASS_$_APMIdentifiers", referenced from:
        _OBJC_METACLASS_$_FIRAIdentifiers in FirebaseAnalytics(FIRAIdentifiers.o)
    "_OBJC_METACLASS_$_APMMeasurement", referenced from:
        _OBJC_METACLASS_$_FIRAMeasurement in FirebaseAnalytics(FIRAMeasurement.o)
    "_OBJC_METACLASS_$_APMScreenViewReporter", referenced from:
        _OBJC_METACLASS_$_FIRAScreenViewReporter in FirebaseAnalytics(FIRAScreenViewReporter.o)
    "_OBJC_METACLASS_$_APMUserAttribute", referenced from:
        _OBJC_METACLASS_$_FIRAUserAttribute in FirebaseAnalytics(FIRAUserAttribute.o)
    "_OBJC_METACLASS_$_APMValue", referenced from:
        _OBJC_METACLASS_$_FIRAValue in FirebaseAnalytics(FIRAValue.o)
  ld: symbol(s) not found for architecture arm64
  clang: error: linker command failed with exit code 1 (use -v to see invocation)
  
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error : clang++ exited with code 1: [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error : ld: warning: Could not find or use auto-linked framework 'GoogleAppMeasurement' [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error : Undefined symbols for architecture arm64: [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :   "_APMAnalyticsConfiguration", referenced from: [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :       +[FIRAnalytics startWithConfiguration:options:] in FirebaseAnalytics(FIRAnalytics.o) [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :   "_APMAppMeasurementOriginFirebase", referenced from: [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :       +[FIRAnalytics startWithConfiguration:options:] in FirebaseAnalytics(FIRAnalytics.o) [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :   "_APMConsentSettings3P", referenced from: [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :       +[FIRAnalytics setConsent:] in FirebaseAnalytics(FIRAnalytics.o) [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :   "_APMFormattedEventName", referenced from: [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :       +[FIRAnalytics logEventWithOrigin:name:parameters:] in FirebaseAnalytics(FIRAnalytics.o) [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :   "_APMFormattedUserPropertyName", referenced from: [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :       +[FIRAnalytics setUserPropertyString:forName:] in FirebaseAnalytics(FIRAnalytics.o) [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :   "_APMIsAnalyticsCollectionDeactivated", referenced from: [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :       +[FIRAnalytics startWithConfiguration:options:] in FirebaseAnalytics(FIRAnalytics.o) [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :   "_APMIsAnalyticsCollectionEnabled", referenced from: [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :       +[FIRAna [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]

Build FAILED.

/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/tools/msbuild/iOS/Xamarin.Shared.targets(146,3): warning : The directory '/Users/miroslavkouril/Library/Caches/XamarinBuildDownload/GAppM-10.24.0/GoogleAppMeasurement-10.24.0/Frameworks' does not exist. [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/Users/miroslavkouril/Library/Caches/XamarinBuildDownload/FAnlytcs-10.24.0/FirebaseAnalytics-10.24.0/Frameworks/FirebaseAnalytics.xcframework/ios-arm64_x86_64-simulator/FirebaseAnalytics.framework/FirebaseAnalytics : warning MT7091: The framework /Users/miroslavkouril/Library/Caches/XamarinBuildDownload/FAnlytcs-10.24.0/FirebaseAnalytics-10.24.0/Frameworks/FirebaseAnalytics.xcframework/ios-arm64_x86_64-simulator/FirebaseAnalytics.framework is a framework of static libraries, and will not be copied to the app. [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error : clang++ exited with code 1: [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error : ld: warning: Could not find or use auto-linked framework 'GoogleAppMeasurement' [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error : Undefined symbols for architecture arm64: [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :   "_APMAnalyticsConfiguration", referenced from: [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :       +[FIRAnalytics startWithConfiguration:options:] in FirebaseAnalytics(FIRAnalytics.o) [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :   "_APMAppMeasurementOriginFirebase", referenced from: [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :       +[FIRAnalytics startWithConfiguration:options:] in FirebaseAnalytics(FIRAnalytics.o) [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :   "_APMConsentSettings3P", referenced from: [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :       +[FIRAnalytics setConsent:] in FirebaseAnalytics(FIRAnalytics.o) [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :   "_APMFormattedEventName", referenced from: [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :       +[FIRAnalytics logEventWithOrigin:name:parameters:] in FirebaseAnalytics(FIRAnalytics.o) [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :   "_APMFormattedUserPropertyName", referenced from: [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :       +[FIRAnalytics setUserPropertyString:forName:] in FirebaseAnalytics(FIRAnalytics.o) [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :   "_APMIsAnalyticsCollectionDeactivated", referenced from: [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :       +[FIRAnalytics startWithConfiguration:options:] in FirebaseAnalytics(FIRAnalytics.o) [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :   "_APMIsAnalyticsCollectionEnabled", referenced from: [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
/usr/local/share/dotnet/packs/Microsoft.iOS.Sdk/17.2.8053/targets/Xamarin.Shared.Sdk.targets(1560,3): error :       +[FIRAna [/Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj::TargetFramework=net8.0-ios]
    2 Warning(s)
    1 Error(s)

Time Elapsed 00:00:13.35

 *  The terminal process "/bin/zsh '-l', '-c', 'dotnet build -t:Build -p:Configuration=Debug -f net8.0-ios -r iossimulator-arm64 -p:CustomAfterMicrosoftCSharpTargets="/Users/miroslavkouril/.vscode/extensions/ms-dotnettools.dotnet-maui-1.0.6-darwin-arm64/dist/resources/Custom.After.Microsoft.CSharp.targets" -p:MauiVSCodeBuildOutputFile="/var/folders/5l/39_hr8w90nx1d4ys4qjzg52h0000gp/T/dotnet-maui/maui-vsc-ca5842d3-6956-4c70-a9d2-a0282f254ae8.json" -p:XamlTools="/Users/miroslavkouril/.vscode/extensions/ms-dotnettools.csharp-2.34.10-darwin-arm64/.xamlTools" /Users/miroslavkouril/Documents/Development/maui-test/ATPWTAJointApp/ATPWTAJointApp.csproj'" terminated with exit code: 1. 
 *  Terminal will be reused by tasks, press any key to close it. 

```

My local env:

```
Visual Studio Community 2022 for Mac
Version 17.6.12 (build 410)
Installation UUID: 334cee1c-2eb7-4d4e-8ebe-146019d00b73

Runtime
.NET 7.0.3 (64-bit)
Architecture: Arm64
Microsoft.macOS.Sdk 13.1.1007; git-rev-head:8afca776a0a96613dfb7200e0917bb57f9ed5583; git-branch:release/7.0.1xx-xcode14.2

Roslyn (Language Service)
4.6.0-3.23180.6+99e956e42697a6dd886d1e12478ea2b27cceacfa

NuGet
Version: 6.4.0.117

.NET SDK (Arm64)
SDK: /usr/local/share/dotnet/sdk/7.0.316/Sdks
SDK Versions:
	8.0.204
	8.0.101
	8.0.100
	7.0.316
	7.0.315
	7.0.312
	7.0.311
	6.0.422
	6.0.421
	6.0.418
	6.0.417
MSBuild SDKs: /Applications/Visual Studio.app/Contents/MonoBundle/MSBuild/Current/bin/Sdks

.NET Runtime (Arm64)
Runtime: /usr/local/share/dotnet/dotnet
Runtime Versions:
	8.0.4
	8.0.1
	8.0.0
	7.0.19
	7.0.18
	7.0.15
	7.0.14
	6.0.30
	6.0.29
	6.0.26
	6.0.25

Xamarin.Profiler
Version: 1.8.0.49
Location: /Applications/Xamarin Profiler.app/Contents/MacOS/Xamarin Profiler

Updater
Version: 11

Xamarin.Android
Version: 13.2.2.0 (Visual Studio Community)
Commit: xamarin-android/d17-5/45b0e14
Android SDK: /Users/miroslavkouril/Library/Developer/Xamarin/android-sdk-macosx
	Supported Android versions:
		12.0 (API level 31)
		13.0 (API level 33)

SDK Command-line Tools Version: 7.0
SDK Platform Tools Version: 35.0.1
SDK Build Tools Version: 34.0.0

Build Information: 
Mono: d9a6e87
Java.Interop: xamarin/java.interop/d17-5@149d70fe
SQLite: xamarin/sqlite/3.40.1@68c69d8
Xamarin.Android Tools: xamarin/xamarin-android-tools/d17-5@ca1552d

Microsoft Build of OpenJDK
Java SDK: /Library/Java/JavaVirtualMachines/microsoft-11.jdk
11.0.16.1
Android Designer EPL code available here:
https://github.com/xamarin/AndroidDesigner.EPL

Eclipse Temurin JDK
Java SDK: /Library/Java/JavaVirtualMachines/temurin-8.jdk
1.8.0.302
Android Designer EPL code available here:
https://github.com/xamarin/AndroidDesigner.EPL

Android SDK Manager
Version: 17.6.0.50
Hash: a715dca
Branch: HEAD
Build date: 2024-05-09 04:36:12 UTC

Android Device Manager
Version: 0.0.0.1309
Hash: 06e3e77
Branch: HEAD
Build date: 2024-05-09 04:36:12 UTC

Apple Developer Tools
Xcode: 15.3 22618
Build: 15E204a

Xamarin.Mac
Not Installed

Xamarin.iOS
Version: 16.4.0.23 Visual Studio Community
Hash: 9defd91b3
Branch: xcode14.3
Build date: 2023-10-23 16:15:00-0400

Xamarin Designer
Version: 17.6.3.9
Hash: 2648399ae8
Branch: remotes/origin/d17-6
Build date: 2024-05-09 04:36:07 UTC

Build Information
Release ID: 1706120410
Git revision: 2f8e0518dd80a933901821bac53f7398d4b61c0f
Build date: 2024-05-09 04:34:23+00
Build branch: release-17.6
Build lane: release-17.6

Operating System
Mac OS X 14.4.1
Darwin 23.4.0 Darwin Kernel Version 23.4.0
    Fri Mar 15 00:10:42 PDT 2024
    root:xnu-10063.101.17~1/RELEASE_ARM64_T6000 arm64
```



