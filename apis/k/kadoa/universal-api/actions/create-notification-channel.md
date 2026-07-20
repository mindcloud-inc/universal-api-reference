# Kadoa: Create Notification Channel



```
POST https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/create-notification-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kadoa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/create-notification-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelType": "WEBHOOK",
  "config": "[object Object]",
  "name": "Test Channel"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/create-notification-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelType": "WEBHOOK",
    "config": "[object Object]",
    "name": "Test Channel"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelType` | string | yes | Type: EMAIL, SLACK, WEBHOOK, WEBSOCKET Default: `WEBHOOK`. |
| `config` | object | yes | JSON config object Example: `[object Object]`. |
| `name` | string | yes | Channel name Default: `Test Channel`. |

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

Through the native Kadoa API, this operation is `POST /v5/notifications/channels` (base URL `https://api.kadoa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-notification-channel.md) for the provider-specific parameters and requirements.

