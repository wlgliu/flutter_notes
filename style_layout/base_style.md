### 设置最大最小宽高
```dart
Container(
    width: 100,
    height: 20,
    constraints: BoxConstraints(
        minWidth: 180,  // 最大高度
        minHeight: 50,  // 最小高度
    ),
    child: Text('Container设置最小宽高'),
)
```

### 设置圆角
* 单个圆角
```dart
borderRadius: BorderRadius.only(topLeft: Radius.circular(5), 
    bottomRight: Radius.circular(20)),
```
* 全部圆角
```dart
borderRadius: BorderRadius.only(topLeft: Radius.circular(5), 
    bottomRight: Radius.circular(20)),
```

### 设置边框
 * 单个边框
 ```dart
border: Border(top: BorderSide(color: Colors.red, width: 2))
 ```
 * 全部边框
 ```dart
border: Border.all(color: Colors.black, width: 2)
 ```

### 过度背景颜色
```dart
decoration: BoxDecoration(
    gradient: LinearGradient(
        begin: Alignment.bottomCenter,
        end: Alignment.topCenter,
        colors: [Color(0xffFA9804), Color(0xffFAC800)],
    ),
),
```

### 添加阴影
```dart
boxShadow: [
    BoxShadow(
        color: Color(0x14000000),
        offset: Offset(0, 4),
        blurRadius: 12.0,
        spreadRadius: 0
    ),
],
```
