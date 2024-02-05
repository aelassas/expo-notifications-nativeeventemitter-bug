# Minimal reproducible example for expo-notifications bug report

All the relevant code is in the App.js file.

App.js is the same as the one in the official [guide](https://docs.expo.dev/versions/latest/sdk/notifications/).

The project was generated as per standard procedure:

```
npx create-expo-app expo-notifications-nativeeventemitter-bug
```

expo-notifications was installed as per standard procedure:

```
npx expo install expo-notifications
```

expo-device was installed as per standard procedure:

```
npx expo install expo-device
```

As long the App is loaded, a couple of warings appears:

```
 WARN  `new NativeEventEmitter()` was called with a non-null argument without the required `addListener` method.
 WARN  `new NativeEventEmitter()` was called with a non-null argument without the required `removeListeners` method.
 WARN  `new NativeEventEmitter()` was called with a non-null argument without the required `addListener` method.
 WARN  `new NativeEventEmitter()` was called with a non-null argument without the required `removeListeners` method.
 WARN  `new NativeEventEmitter()` was called with a non-null argument without the required `addListener` method.
 WARN  `new NativeEventEmitter()` was called with a non-null argument without the required `removeListeners` method.
```

On the device we can see that the warnings occure in:
```
node_modules/expo-notifications/build/index.js
```
