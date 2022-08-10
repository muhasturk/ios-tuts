# 003-Navigation Bar Color in SwiftUI on iOS 16

We can use new [API](https://developer.apple.com/documentation/swiftui/view/toolbarbackground(_:for:)-5ybst)

## Declaration
```swift
func toolbarBackground(
    _ visibility: Visibility,
    for bars: ToolbarPlacement...
) -> some View
```

## Example
```swift
struct ContentView: View {
    var body: some View {
        NavigationStack {
            List {
                Text("Mustafa Hasturk")
            }
            .navigationTitle("Navigation Title")
            .toolbarBackground(
                Color.red,
                in: .navigationBar)
        }
    }
}
```

### Visibility
```swift
.toolbarBackground(.visible, in: .navigationBar)`
```
