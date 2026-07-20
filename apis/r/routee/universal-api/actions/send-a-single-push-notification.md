# Routee: Send a Single Push Notification

Sends a single push notification with Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-single-push-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-single-push-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "implementationId": "string",
  "deviceToken": {},
  "deviceToken.type": "string",
  "deviceToken.token": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-single-push-notification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "implementationId": "string",
    "deviceToken": {},
    "deviceToken.type": "string",
    "deviceToken.token": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `implementationId` | string | yes | There should be an implementation with the particular id that belongs to the accountId. Not blank. |
| `deviceToken` | object | yes | Device token. It is used to identify a specific device. |
| `deviceToken.type` | string | yes | Device token type: ANDROID, APPLE, WEB. |
| `deviceToken.token` | string | yes | Not blank. |
| `body` | object | no | The notification's body which contains the following fields: title, text, forceLocale. |
| `body.title` | object | no | The notification's title. Map: (Key) not blank, language - ISO 639-1; (Value) not blank. |
| `body.text` | object | no | The notification's text. Map: (Key) not blank, language - ISO 639-1; (Value) not blank. |
| `body.forceLocale` | string | no | Localization settings. Switches body.title and body.text to the selected language; body.title and body.text should contain an entry with forceLocale as their key. Not null, language - ISO 639-1. |
| `imageUrl` | string | no | URL that should begin with https:// |
| `android` | object | no | Device-specific parameters (Android). |
| `android.clickAction` | string | no | The action associated with a user click on the notification. |
| `android.icon` | string | no | The notification's icon. Sets the notification icon to myicon for drawable resource myicon. If you don't send this key in the request, FCM displays the launcher icon specified in your app manifest. |
| `android.localizedTitle` | string | no | The key to the title string in the app's string resources to use to localize the title text to the user's current localization. Example: NOTIFICATION_TITLE. |
| `android.localizedText` | string | no | The key to the body string in the app's string resources to use to localize the body text to the user's current localization. Example: NOTIFICATION_MESSAGE. |
| `android.ttl` | number | no | In seconds. Min: 0. Max: 2.419.200. Default: same as Firebase (current: 2.419.200). |
| `apn` | object | no | Device-specific parameters (iOS). |
| `apn.localizedTitle` | string | no | The key for a localized title string. Specify this key instead of the title key to retrieve the title from your app's Localizable.strings files. The value must contain the name of a key in your strings file. |
| `apn.localizedText` | string | no | The key for a localized message string. Use this key, instead of the body key, to retrieve the message text from your app's Localizable.strings file. The value must contain the name of a key in your strings file. |
| `apn.ttl` | number | no | In seconds. Min: 0. Max: 2.419.200. Default: same as Firebase (current: 2.419.200). |
| `web` | object | no | Device-specific parameters (web). |
| `web.iconUrl` | string | no | URL that should begin with https:// |
| `web.targetUrl` | string | no | URL that should begin with https:// |
| `data` | object | no | This parameter specifies the custom key-value pairs of the message's payload. For example, with data:{"score":"3x1"}: On Apple platforms, if the message is sent via APNs, it represents the custom data fields. If it is sent via FCM, it would be represented as key value dictionary in AppDelegate application:didReceiveRemoteNotification:. On Android, this would result in an intent extra named score with the string value 3x1. The key should not be a reserved word ("from", "message_type", or any word starting with "google" or "gcm"). Values should be string type. |
| `data.key` | string | no | Not blank. |
| `data.value` | string | no | Not blank. |
| `callbackUrl` | string | no | URL that should begin with https:// |

## Response

```json
{
  "success": true,
  "data": [
    {
      "trackingId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `trackingId` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /push-notifications/messages` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-a-single-push-notification.md) for the provider-specific parameters and requirements.

