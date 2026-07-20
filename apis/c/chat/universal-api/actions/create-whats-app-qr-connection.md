# 2Chat: Create WhatsApp QR Connection

Creates a WhatsApp QR connection in 2Chat.

```
POST https://connect.mindcloud.co/v1/universal/chat/latest/actions/create-whats-app-qr-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chat/latest/actions/create-whats-app-qr-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phoneNumber": "string",
  "friendlyName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chat/latest/actions/create-whats-app-qr-connection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phoneNumber": "string",
    "friendlyName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phoneNumber` | string | yes | The WhatsApp phone number to connect to 2Chat. |
| `friendlyName` | string | yes | A friendly label for the connected number. |

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

Through the native 2Chat API, this operation is `POST /whatsapp/channel/create` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-whats-app-qr-connection.md) for the provider-specific parameters and requirements.

