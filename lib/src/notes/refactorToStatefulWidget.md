### Refactoring to a Stateful Widget
#### Steps:
 - Break the widget into two separate classes, the **_Widget_** and the **_Widget's State_**
- Add a **`createState`** method to the **_Widget_** class that *returns* an instance of **_Widget State_**
- Add a **_build_** method to the **_Widget State_** class
- Add **_instance variables_** to the **_Widget State_** class
- Any time the *Widget State* class's data changes, call the _'setState'_ method