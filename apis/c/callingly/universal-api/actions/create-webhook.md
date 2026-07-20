# Callingly: Create Webhook

Creates a webhook in Callingly.

```
POST https://connect.mindcloud.co/v1/universal/callingly/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callingly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/callingly/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud Test Webhook",
  "event": "lead_created",
  "targetUrl": "https://example.com/mindcloud/callingly-webhook"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callingly/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud Test Webhook",
    "event": "lead_created",
    "targetUrl": "https://example.com/mindcloud/callingly-webhook"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Example: `MindCloud Test Webhook`. |
| `event` | string | yes | Example: `lead_created`. |
| `targetUrl` | string | yes | Example: `https://example.com/mindcloud/callingly-webhook`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callDirection` | string | no | Example: `outbound`. |
| `callStatus` | string | no | Example: `completed`. |
| `callLeadStatus` | string | no | Example: `contacted`. |
| `teamId` | number | no | Example: `19230`. |
| `numberId` | number | no | Example: `123`. |
| `field` | string | no | Example: `stage`. |
| `filter` | string | no | Example: `called`. |

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

Through the native Callingly API, this operation is `POST /v1/webhooks` (base URL `https://api.callingly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

