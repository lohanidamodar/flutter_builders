# Flutter JSON to Widget generator

Automatically generate Widgets from JSON templates using flutter builders.

## Example
- JSON Schema
    ```json
    {
        "name":"Container",
        "params": {
            "color":"#Color(0xffff0000)",
            "padding":"#const EdgeInsets.all(16.0)",
            "child": {
                "name":"Text",
                "params":{
                    "0": "Hello flutter builder!",
                    "style":"#TextStyle(color: Color(0xffffffff), fontWeight: FontWeight.bold )"
                }
            }
        }
    }
    ```
- Generated Code
    ```dart
    //generated code
    import 'package:flutter/widgets.dart';

    class GeneratedWidget extends StatelessWidget {
    @override
    Widget build(BuildContext context) {
        return Container(
        color: Color(0xffff0000),
        padding: const EdgeInsets.all(16.0),
        child: Text(
            "Hello flutter builder!",
            style: TextStyle(color: Color(0xffffffff), fontWeight: FontWeight.bold),
        ),
        );
    }
    }

    ```


## Getting Started with flutter

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
