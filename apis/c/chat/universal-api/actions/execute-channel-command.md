# 2Chat: Execute Channel Command

Updates a WhatsApp channel in 2Chat with a command.

```
PUT https://connect.mindcloud.co/v1/universal/chat/latest/actions/execute-channel-command
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chat/latest/actions/execute-channel-command" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channel_uuid": "string",
  "command": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chat/latest/actions/execute-channel-command', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channel_uuid": "string",
    "command": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channel_uuid` | string | yes | The UUID of the WhatsApp channel connected to 2Chat. |
| `command` | string | yes | The command to execute for the channel, such as connect or disconnect. |

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

Through the native 2Chat API, this operation is `POST /whatsapp/channel/:channel_uuid/:command` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-channel-command.md) for the provider-specific parameters and requirements.

