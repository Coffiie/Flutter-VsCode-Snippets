# Flutter-VsCode-Snippets
A repository where I keep track of my VS Code / Flutter snippets for Flutter/Dart so I can set them in a new environment if need be.

## **Getter and Setter with notifyListeners**

This saves time by setting up the required datatype, public and private variables without having to type them out. A must use if you use notifyListeners() in your setters as well. You can modify the prefixes to fit your needs

    "Getter and Setter with notifyListeners": {
    "prefix": ["getter","get","ge","g","s","set","se","setter"],
    "body": ["${0:DataType} ${1:privVar}; ${0:DataType} get ${2:pubVar} => ${1:privVar}; set ${2:pubVar}(${0:DataType} val){ ${1:privVar} = val; notifyListeners(); }"],
    }
