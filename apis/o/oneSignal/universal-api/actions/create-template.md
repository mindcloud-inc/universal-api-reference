# OneSignal: Create Template

Creates a template in OneSignal.

```
POST https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contents": {},
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contents": {},
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contents` | object | yes | Localized template contents keyed by language code, such as {"en":"Hello from OneSignal"}. |
| `name` | string | yes | A name for the template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "content": {
        "contents": {
          "en": "string"
        },
        "disableEmailClickTracking": {},
        "emailBody": {},
        "emailPreheader": {},
        "emailReplyToAddress": {},
        "emailSubject": {},
        "globalImage": {},
        "huaweiBadgeAddNum": {},
        "huaweiBadgeClass": {},
        "huaweiBadgeSetNum": {},
        "isAdm": true,
        "isAlexa": {},
        "isAndroid": true,
        "isChrome": true,
        "isChromeWeb": true,
        "isEdge": true,
        "isEmail": {},
        "isFirefox": true,
        "isHuawei": true,
        "isIos": true,
        "isMacOSX": true,
        "isSafari": true,
        "isSMS": {},
        "isWP": true,
        "isWPWNS": true,
        "smsFrom": {},
        "smsMediaUrls": {},
        "subtitle": {},
        "url": {}
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `content.contents.en` | string |  |
| `content.disableEmailClickTracking` | object |  |
| `content.emailBody` | object |  |
| `content.emailPreheader` | object |  |
| `content.emailReplyToAddress` | object |  |
| `content.emailSubject` | object |  |
| `content.globalImage` | object |  |
| `content.huaweiBadgeAddNum` | object |  |
| `content.huaweiBadgeClass` | object |  |
| `content.huaweiBadgeSetNum` | object |  |
| `content.isAdm` | boolean |  |
| `content.isAlexa` | object |  |
| `content.isAndroid` | boolean |  |
| `content.isChrome` | boolean |  |
| `content.isChromeWeb` | boolean |  |
| `content.isEdge` | boolean |  |
| `content.isEmail` | object |  |
| `content.isFirefox` | boolean |  |
| `content.isHuawei` | boolean |  |
| `content.isIos` | boolean |  |
| `content.isMacOSX` | boolean |  |
| `content.isSafari` | boolean |  |
| `content.isSMS` | object |  |
| `content.isWP` | boolean |  |
| `content.isWPWNS` | boolean |  |
| `content.smsFrom` | object |  |
| `content.smsMediaUrls` | object |  |
| `content.subtitle` | object |  |
| `content.url` | object |  |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native OneSignal API, this operation is `POST /templates` (base URL `https://api.onesignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

