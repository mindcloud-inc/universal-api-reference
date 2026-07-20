# Lulu: Get Webhook

Retrieves a webhook from Lulu.

```
GET https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lulu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-webhook?connectionId=$CONNECTION_ID&id=6b522ab9-31ec-4418-a904-95436160d4a8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "6b522ab9-31ec-4418-a904-95436160d4a8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-webhook?${params}`, {
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
| `id` | string | yes | Lulu webhook ID. Default: `6b522ab9-31ec-4418-a904-95436160d4a8`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "isActive": true,
      "topics": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isActive` | boolean |  |
| `topics` | array<string> |  |
| `url` | string |  |

## Native endpoint

Through the native Lulu API, this operation is `GET /webhooks/{id}/` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

