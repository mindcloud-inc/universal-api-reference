# Callingly: Get Webhook

Retrieves a webhook from Callingly.

```
GET https://connect.mindcloud.co/v1/universal/callingly/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callingly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callingly/latest/actions/get-webhook?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callingly/latest/actions/get-webhook?${params}`, {
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
| `id` | number | yes | The Callingly webhook ID to retrieve. |

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

Through the native Callingly API, this operation is `GET /v1/webhooks/{{id}}` (base URL `https://api.callingly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

