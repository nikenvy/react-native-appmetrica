# react-native-appmetrica

React Native bridge to the [AppMetrica](https://appmetrica.yandex.com/) on both iOS and Android.

## Installation

```sh
yarn add https://github.com/nikenvy/react-native-appmetrica
```

add to Podile

```sh
  pod 'react-native-appmetrica-yandex', :path => '../node_modules/react-native-appmetrica-yandex'
```

## Usage

```js
import { YandexMetrica } from 'react-native-appmetrica-yandex';

// Initialize
YandexMetrica.activateWithApiKey('KEY');

// OR
YandexMetrica.activateWithConfig({
  apiKey: 'KEY',
  sessionTimeout: 120,
  firstActivationAsUpdate: true,
});


YandexMetrica.setUserProfileID('12345');

YandexMetrica.setUserProfileAttributes({ ... })

// Sends a custom event message and additional parameters (optional).
YandexMetrica.reportEvent('My event');
YandexMetrica.reportEvent('My event', 'Test');
YandexMetrica.reportEvent('My event', { foo: 'bar' });

// Send a custom error event and additional parameters (optional).
YandexMetrica.reportError('My error');
YandexMetrica.reportError('My error', 'Test');
YandexMetrica.reportError('My error', { foo: 'bar' });
YandexMetrica.reportError('My error', new Error('test'));


// Send a custom report app open via deeplink.
YandexMetrica.reportAppOpen(deeplink);
```
