# Helpjuice: Get Webhook

Retrieves a webhook from Helpjuice.

```
GET https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Helpjuice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/get-webhook?connectionId=$CONNECTION_ID&webhookId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/get-webhook?${params}`, {
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
| `webhookId` | number | yes | The Helpjuice webhook id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "created_at": "string",
      "created_by_id": 1,
      "enabled_at": "string",
      "event": "string",
      "id": 1,
      "last_response_code": 1,
      "updated_at": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `created_at` | string |  |
| `created_by_id` | number |  |
| `enabled_at` | string |  |
| `event` | string |  |
| `id` | number |  |
| `last_response_code` | number |  |
| `updated_at` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Helpjuice API, this operation is `GET /webhooks/:id` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

