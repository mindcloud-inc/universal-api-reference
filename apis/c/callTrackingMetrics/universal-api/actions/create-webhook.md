# CallTrackingMetrics: Create Webhook

Creates a new webhook in CallTrackingMetrics.

```
POST https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallTrackingMetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "weburl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "weburl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `weburl` | string | yes | The destination URL for CTM webhook delivery. |
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
        "weburl": "https://example.com",
        "withResourceUrl": true
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
| `webhook.withResourceUrl` | boolean |  |

## Native endpoint

Through the native CallTrackingMetrics API, this operation is `POST /accounts/:accountId/webhooks` (base URL `https://api.calltrackingmetrics.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

