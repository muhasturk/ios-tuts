In order to improve the readability of the numeric literals.

These extra formatting has no affects on the underlying value for [Numeric literals](https://docs.swift.org/swift-book/LanguageGuide/TheBasics.html#ID323)

- Underscores (_)
- Leading zeros

### Large Number
```swift
let baseValue = 1_000_000 // 1000000
let expected = 1_000_000.000_000_1 // 10000000.0000001

let isGreater = expeced > baseValue
```

### HEX Number

```swift
let red = 0xff0000
let sameRed = 0xff_00_00
```

### Alignment

```swift
let aWeight = 0.123
let bWeight = 12345
```

```swift
let aWeight = 00000.123
let bWeight = 12345.000
```
