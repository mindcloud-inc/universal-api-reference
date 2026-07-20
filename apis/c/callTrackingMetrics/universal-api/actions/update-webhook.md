# CallTrackingMetrics: Update Webhook

Updates an existing webhook in CallTrackingMetrics.

```
PUT https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallTrackingMetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookId` | string | yes | The CallTrackingMetrics webhook ID. |
| `weburl` | string | no | The destination URL for CTM webhook delivery. |
| `hooktype` | string | no | Optional webhook trigger type. |
| `position` | string | no | The CTM webhook position enum value. |
| `name` | string | no | Optional CTM webhook display name. |
| `username` | string | no | Optional HTTP basic username CTM should send to the webhook endpoint. |
| `password` | string | no | Optional HTTP basic password CTM should send to the webhook endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "warnings": {},
      "webhook": {
        "accountId": 1,
        "clientId": 1,
        "clientType": "string",
        "id": 1,
        "name": "Ava Chen",
        "position": "string",
        "weburl": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `warnings` | object |  |
| `webhook` | object |  |
| `webhook.accountId` | number |  |
| `webhook.clientId` | number |  |
| `webhook.clientType` | string |  |
| `webhook.id` | number |  |
| `webhook.name` | string |  |
| `webhook.position` | string |  |
| `webhook.weburl` | string |  |

## Native endpoint

Through the native CallTrackingMetrics API, this operation is `PUT /accounts/:accountId/webhooks/:webhookId` (base URL `https://api.calltrackingmetrics.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

