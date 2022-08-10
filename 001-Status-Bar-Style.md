# 001-Status Bar Style

## View controller-based

- Set `View controller-based status bar appearance` - `YES`. If not defined default value is `YES`
```xml
<key>UIViewControllerBasedStatusBarAppearance</key>
<true/>
```

- Override properties in VC
```swift
override var preferredStatusBarStyle: UIStatusBarStyle {
    .lightContent
}
```

- If embedded your VC in NVC / TabBarController, override

#### Use Case 1: Set Default Style For All
```swift
override var preferredStatusBarStyle: UIStatusBarStyle {
    .lightContent
}
```

#### Use Case 2: In order to apply VC's style
```swift
override var childForStatusBarStyle: UIViewController? {
    visibleViewController
}
```

> Call `setNeedsStatusBarAppearanceUpdate()` if preferredStatusBarStyle value is going to be changed

## App Based

Apply both

- Set `View controller-based status bar appearance` - `NO`
```xml
<key>UIViewControllerBasedStatusBarAppearance</key>
<true/>
```

- Set `Status bar style` to desired value
```xml
<key>UIStatusBarStyle</key>
<string>UIStatusBarStyleDarkContent</string>
```

## SwiftUI

⚠️ Need more API

We can not override the status bar per view.
```swift
.preferredColorScheme(.dark)
```

### (iOS 16)
```swift
.toolbarColorScheme(.light, in: .navigationBar)
```
