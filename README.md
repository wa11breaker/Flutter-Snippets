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
