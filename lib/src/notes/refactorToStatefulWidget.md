## Main Concepts in this App =>
### Refactoring to a Stateful Widget =>
 - Break the widget into two separate classes, the **_Widget_** and the **_Widget's State_**
- Add a **`createState`** method to the **_Widget_** class that *returns* an instance of **_Widget State_**
- Add a **_build_** method to the **_Widget State_** class
- Add **_instance variables_** to the **_Widget State_** class
- Any time the *Widget State* class's data changes, call the _'setState'_ method

### Import Statements =>
- From another **_package_** => `import 'package:flutter/material.dart';`
- From another **_file_** => `import 'models/image_model.dart';`
- From **_Dart_** standard library => `import 'dart:convert';`

### Difference Between Stateless and Stateful Widgets =>
- *Stateless Widgets* are for presentation and used when we want to take data and render it on screen. Any time this widget's state changes we take the original widget and throw it away and render a new one with new data. This is where the `Final` type comes in.
-  *Stateful Widgets* have data that we don't want to throw away. This still places a widget in the widget tree and has `createState` called on it which controls the state outside of our widget tree and preserves the data.

### Async Code Handling in Dart =>
- This uses the `async/await` syntax to wait for the `Future` which gets returned from the `fetchImage()` method in `app.dart`. Once this resolves we then use our `ImageModel` inside the `SetState()` method to cause our Widget to re-render and show new data.

#### Notes =>
 - This idea of Stateful and Stateless Widgets in Flutter is just one pattern of State Management in Flutter and is the recommended pattern for handling state in Flutter from the Authors of Flutter.  There are other Patterns recommended