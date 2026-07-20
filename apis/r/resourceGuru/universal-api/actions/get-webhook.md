# Resource Guru: Get Webhook

Retrieves a webhook from Resource Guru.

```
GET https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resource Guru `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/get-webhook?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/get-webhook?${params}`, {
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
| `id` | number | yes | Webhook ID. Default: `1`. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "id": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | Webhook creation timestamp. |
| `id` | number | Webhook ID. |
| `url` | string | Webhook target URL. |

## Native endpoint

Through the native Resource Guru API, this operation is `GET /webhooks/:id` (base URL `https://api.resourceguruapp.com/v1/{{credentials.accountId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

