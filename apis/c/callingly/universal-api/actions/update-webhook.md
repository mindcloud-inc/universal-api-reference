# Callingly: Update Webhook

Updates a webhook in Callingly.

```
PUT https://connect.mindcloud.co/v1/universal/callingly/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callingly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/callingly/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "webhookId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callingly/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "webhookId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callDirection` | string | no | The call direction filter. |
| `callLeadStatus` | string | no | The call lead status filter. |
| `callStatus` | string | no | The call status filter. |
| `event` | string | no | The webhook event type. |
| `field` | string | no | Only trigger when this lead field changes. |
| `filter` | string | no | Only trigger when the selected field matches this value. |
| `id` | number | yes | The Callingly webhook ID to update. |
| `name` | string | no | The webhook name. |
| `numberId` | number | no | The number ID filter. |
| `targetUrl` | string | no | The webhook destination URL. |
| `teamId` | number | no | The team ID filter. |
| `webhookId` | number | yes | The Callingly webhook ID to update in the path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "call_lead_status": "string",
      "call_status": "string",
      "direction": "string",
      "event": "string",
      "field": "string",
      "filter": "string",
      "id": 1,
      "name": "Ava Chen",
      "number_id": 1,
      "target_url": "https://example.com",
      "team_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `call_lead_status` | string |  |
| `call_status` | string |  |
| `direction` | string |  |
| `event` | string |  |
| `field` | string |  |
| `filter` | string |  |
| `id` | number |  |
| `name` | string |  |
| `number_id` | number |  |
| `target_url` | string |  |
| `team_id` | number |  |

## Native endpoint

Through the native Callingly API, this operation is `PUT /v1/webhooks/{{webhookId}}` (base URL `https://api.callingly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

