# Kadoa: Update Notification Channel



```
PUT https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/update-notification-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kadoa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/update-notification-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "channelType": "string",
  "config": {},
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/update-notification-channel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "channelType": "string",
    "config": {},
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | Channel ID |
| `channelType` | string | yes | Type: EMAIL, SLACK, WEBHOOK, WEBSOCKET |
| `config` | object | yes | JSON config object |
| `name` | string | yes | Channel name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "channel": {
          "channelType": "string",
          "config": {},
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "name": "Ava Chen",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.channel.channelType` | string |  |
| `data.channel.config` | object |  |
| `data.channel.createdAt` | date |  |
| `data.channel.id` | string |  |
| `data.channel.name` | string |  |
| `data.channel.updatedAt` | date |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Kadoa API, this operation is `PUT /v5/notifications/channels/:channelId` (base URL `https://api.kadoa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-notification-channel.md) for the provider-specific parameters and requirements.

