# Mifiel: List Webhooks

Retrieves webhook endpoint records from Mifiel.

```
GET https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mifiel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/list-webhooks?${params}`, {
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
      "callback_type": "string",
      "created_at": "string",
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callback_type` | string | Type of events that trigger this webhook |
| `created_at` | string | When webhook was created |
| `id` | string | Unique identifier |
| `url` | string | Webhook URL endpoint |

## Native endpoint

Through the native Mifiel API, this operation is `GET /api/v1/webhooks` (base URL `https://app.mifiel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

