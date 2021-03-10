### 设置最大最小宽高
```dart
Container(
  width: 100,
  height: 100,
  constraints: BoxConstraints(
    maxWidth: 50,
    minHeight: 50,
  ),
  color: Colors.blue,
),
```

### 设置圆角
* 单个圆角
```dart
borderRadius: BorderRadius.only(topLeft: Radius.circular(5)),
```
* 全部圆角
```dart
borderRadius: BorderRadius.all(Radius.circular(5))
```

### 设置边框
 * 单个边框
 ```dart
border: Border(top: BorderSide(width: 1, color: Colors.blue[600],))
 ```
 * 全部边框
 ```dart
border: Border.all(width: 1, color: Colors.blue[600],),
 ```

### 过度背景颜色
* 线性渐变
```dart
gradient: LinearGradient( // 线性渐变
    begin: Alignment.topCenter,
    end: Alignment.bottomCenter,
    colors: [
        Colors.blue[500],
        Colors.blue[300],
        Colors.blue[100],
]),
```
* 径向渐变
```dart
gradient: RadialGradient( // 径向渐变
    colors: [
        Colors.blue[500],
        Colors.blue[300],
        Colors.blue[100],
]),
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

### 添加背景图片
```dart
// 网路链接
decoration: BoxDecoration(
  image: DecorationImage(
    image: NetworkImage(
      item['vertical_src']
    ),
    fit: BoxFit.cover,
  ),
),

// 本地图片
decoration: BoxDecoration(
    image: DecorationImage(
        image: AssetImage('images/home/search_icon_xx.png'),
        fit: BoxFit.cover,
    )
),

// 背景图片添加圆角
ClipRRect( //剪裁为圆角矩形
    borderRadius: BorderRadius.circular(5.0),
    child: Image.asset("imgs/avatar.png", width: 60.0),
),
ClipOval(child: avatar), //剪裁为圆形

// 淡出
FadeInImage.assetNetwork(
    placeholder: 'local',
    image: 'remote',
    fit: BoxFit.cover,
)
```

### 文字超出以...显示
```dart
child: Text(
    '根据其商标申请，“Pl视频游戏活动、会',
    overflow: TextOverflow.ellipsis,    // 以点点点显示
    maxLines: 2,        // 行数
    style: TextStyle(
        fontSize: 10,
        color: Color(0xff222222),
    ),
),
```
