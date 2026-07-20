# Callingly: List Webhooks

Retrieves webhooks from Callingly.

```
GET https://connect.mindcloud.co/v1/universal/callingly/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callingly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callingly/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callingly/latest/actions/list-webhooks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Callingly API, this operation is `GET /v1/webhooks` (base URL `https://api.callingly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

