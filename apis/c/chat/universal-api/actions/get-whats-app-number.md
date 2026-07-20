# 2Chat: Get WhatsApp Number

Retrieves a WhatsApp number from 2Chat.

```
GET https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-whats-app-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-whats-app-number?connectionId=$CONNECTION_ID&channel_uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channel_uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-whats-app-number?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channel_uuid` | string | yes | The UUID of the WhatsApp channel connected to 2Chat. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": {
        "channelType": "string",
        "connectionStatus": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "enabled": true,
        "friendlyName": "Ava Chen",
        "id": "string",
        "isBusinessProfile": true,
        "isoCountryCode": "string",
        "lang": "string",
        "phoneNumber": "string",
        "platform": {},
        "pushname": {},
        "server": {},
        "syncContacts": true,
        "timezone": "string",
        "timezonePhoneNumber": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "uuid": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel.channelType` | string |  |
| `channel.connectionStatus` | string |  |
| `channel.createdAt` | date |  |
| `channel.enabled` | boolean |  |
| `channel.friendlyName` | string |  |
| `channel.id` | string |  |
| `channel.isBusinessProfile` | boolean |  |
| `channel.isoCountryCode` | string |  |
| `channel.lang` | string |  |
| `channel.phoneNumber` | string |  |
| `channel.platform` | object |  |
| `channel.pushname` | object |  |
| `channel.server` | object |  |
| `channel.syncContacts` | boolean |  |
| `channel.timezone` | string |  |
| `channel.timezonePhoneNumber` | string |  |
| `channel.updatedAt` | date |  |
| `channel.uuid` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native 2Chat API, this operation is `GET /whatsapp/channel/:channel_uuid` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-whats-app-number.md) for the provider-specific parameters and requirements.

