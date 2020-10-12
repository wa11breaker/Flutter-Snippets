# Flutter Snippets

##### Check Internet Connectivity
#
```dart
import 'dart:io';
try {
  final result = await InternetAddress.lookup('google.com');
  if (result.isNotEmpty && result[0].rawAddress.isNotEmpty) {
    print('connected');
  }
} on SocketException catch (_) {
  print('not connected');
}
```
##### Change color of CircularProgressIndicator
#
```dart
CircularProgressIndicator(
     valueColor: new AlwaysStoppedAnimation<Color>(Colors.blue),
),
```
 ###### Using Theme Widget
 #
  ```flutter
 Theme(
      data: Theme.of(context).copyWith(accentColor: Colors.red),
      child: new CircularProgressIndicator(),
)
```
 ##### TextField search delay
 ```dart
 TextEditingController _controller = TextEditingController();
 Timer timer;

 _controller.addListener(() {
  if (!_controller.text.isEmpty) {
    if (timer != null) {
      timer.cancel();
      timer = null;
    }
    timer = Timer(Duration(seconds: 1), httpCall);
  }
});

httpCall() {
  try {
    print(_controller.text);
  } catch (_) {}
}
 ```
