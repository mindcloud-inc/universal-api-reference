# eSign Genie: Update Webhook Channel

Updates an existing webhook channel in eSign Genie.

```
PUT https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/update-webhook-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eSign Genie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/update-webhook-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/update-webhook-channel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": {
        "channelId": 1,
        "channelName": "Ava Chen",
        "status": "string",
        "webhookUrl": "https://example.com"
      },
      "message": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel.channelId` | number |  |
| `channel.channelName` | string |  |
| `channel.status` | string |  |
| `channel.webhookUrl` | string |  |
| `message` | string |  |
| `result` | string |  |

## Native endpoint

Through the native eSign Genie API, this operation is `POST /webhook/updatewebhookchannel` (base URL `https://na1.foxitesign.foxit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook-channel.md) for the provider-specific parameters and requirements.

