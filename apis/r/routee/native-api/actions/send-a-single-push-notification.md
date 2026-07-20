# Send a Single Push Notification with Routee

Sends a single push notification with Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/push-notifications/messages`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Send a Single Push Notification](https://docs.routee.net/reference/send-a-single-push-notification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `implementationId` | body | `string` | yes | There should be an implementation with the particular id that belongs to the accountId. Not blank. |
| `deviceToken` | body | `object` | yes | Device token. It is used to identify a specific device. |
| `deviceToken.type` | body | `string` | yes | Device token type: ANDROID, APPLE,  WEB. |
| `deviceToken.token` | body | `string` | yes | Not blank. |
| `body` | body | `object` | no | The notification's body which contains the following fields: title, text, forceLocale. |
| `body.title` | body | `object` | no | The notification's title. Map: (Key) not blank, language - ISO 639-1; (Value) not blank. |
| `body.text` | body | `object` | no | The notification's text. Map: (Key) not blank, language - ISO 639-1; (Value) not blank. |
| `body.forceLocale` | body | `string` | no | Localization settings. Switches body.title and body.text to the selected language; body.title and body.text should contain an entry with forceLocale as their key. Not null, language - ISO 639-1. |
| `imageUrl` | body | `string` | no | URL that should begin with https:// |
| `android` | body | `object` | no | Device-specific parameters (Android). |
| `android.clickAction` | body | `string` | no | The action associated with a user click on the notification. |
| `android.icon` | body | `string` | no | The notification's icon. Sets the notification icon to myicon for drawable resource myicon. If you don't send this key in the request, FCM displays the launcher icon specified in your app manifest. |
| `android.localizedTitle` | body | `string` | no | The key to the title string in the app's string resources to use to localize the title text to the user's current localization. Example: NOTIFICATION_TITLE. |
| `android.localizedText` | body | `string` | no | The key to the body string in the app's string resources to use to localize the body text to the user's current localization. Example: NOTIFICATION_MESSAGE. |
| `android.ttl` | body | `number` | no | In seconds. Min: 0. Max: 2.419.200. Default: same as Firebase (current: 2.419.200). |
| `apn` | body | `object` | no | Device-specific parameters (iOS). |
| `apn.localizedTitle` | body | `string` | no | The key for a localized title string. Specify this key instead of the title key to retrieve the title from your app's Localizable.strings files. The value must contain the name of a key in your strings file. |
| `apn.localizedText` | body | `string` | no | The key for a localized message string. Use this key, instead of the body key, to retrieve the message text from your app's Localizable.strings file. The value must contain the name of a key in your strings file. |
| `apn.ttl` | body | `number` | no | In seconds. Min: 0. Max: 2.419.200. Default: same as Firebase (current: 2.419.200). |
| `web` | body | `object` | no | Device-specific parameters (web). |
| `web.iconUrl` | body | `string` | no | URL that should begin with https:// |
| `web.targetUrl` | body | `string` | no | URL that should begin with https:// |
| `data` | body | `object` | no | This parameter specifies the custom key-value pairs of the message's payload. For example, with data:{"score":"3x1"}: On Apple platforms, if the message is sent via APNs, it represents the custom data fields. If it is sent via FCM, it would be represented as key value dictionary in AppDelegate application:didReceiveRemoteNotification:. On Android, this would result in an intent extra named score with the string value 3x1. The key should not be a reserved word ("from", "message_type", or any word starting with "google" or "gcm"). Values should be string type. |
| `data.key` | body | `string` | no | Not blank. |
| `data.value` | body | `string` | no | Not blank. |
| `callbackUrl` | body | `string` | no | URL that should begin with https:// |
