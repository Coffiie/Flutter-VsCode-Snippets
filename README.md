# Flutter-VsCode-Snippets
A repository where I keep track of my VS Code / Flutter snippets for Flutter/Dart so I can set them in a new environment if need be.

# VS - Code Snippets

### 1. Getter and Setter with notifyListeners

This saves time by setting up the required datatype, public and private variables without having to type them out. A must use if you use notifyListeners() in your setters as well. You can modify the prefixes to fit your needs

    "Getter and Setter with notifyListeners": {
    "prefix": ["getter","get","ge","g","s","set","se","setter"],
    "body": ["${0:DataType} ${1:privVar}; ${0:DataType} get ${2:pubVar} => ${1:privVar}; set ${2:pubVar}(${0:DataType} val){ ${1:privVar} = val; notifyListeners(); }"],
    }

# Flutter / Dart Snippets

### 1. Get Google Map Markers from Image Assets

```dart
static Future<BitmapDescriptor> getMarkerFromAsset(String path) async {
    ByteData data = await rootBundle.load(path);
    ui.Codec codec = await ui.instantiateImageCodec(data.buffer.asUint8List(),
        targetWidth: 45);
    ui.FrameInfo fi = await codec.getNextFrame();
    return BitmapDescriptor.fromBytes(
        (await fi.image.toByteData(format: ui.ImageByteFormat.png))
            .buffer
            .asUint8List());
  }
```
