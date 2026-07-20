# Tolq: Get Translation Request

Retrieves a translation request from Tolq.

```
GET https://connect.mindcloud.co/v1/universal/tolq/latest/actions/get-translation-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tolq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tolq/latest/actions/get-translation-request?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tolq/latest/actions/get-translation-request?${params}`, {
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
| `id` | number | yes | Tolq translation request ID. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "callback_response_code": 1,
      "completed_at": "2026-05-07T12:00:00.000Z",
      "context_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "last_callback_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "orders": [
        {}
      ],
      "original": {},
      "quality": "string",
      "slug": "string",
      "source_language_code": "string",
      "status": "string",
      "style_guide_reference_id": 1,
      "target_language_code": "string",
      "total_cost": 1,
      "total_keys": 1,
      "total_ordered_words": 1,
      "total_orders": 1,
      "total_words": 1,
      "translations": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object |  |
| `callback_response_code` | number |  |
| `completed_at` | date |  |
| `context_url` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `id` | number |  |
| `last_callback_at` | date |  |
| `name` | string |  |
| `orders` | array<object> |  |
| `original` | object |  |
| `quality` | string |  |
| `slug` | string |  |
| `source_language_code` | string |  |
| `status` | string |  |
| `style_guide_reference_id` | number |  |
| `target_language_code` | string |  |
| `total_cost` | number |  |
| `total_keys` | number |  |
| `total_ordered_words` | number |  |
| `total_orders` | number |  |
| `total_words` | number |  |
| `translations` | object |  |

## Native endpoint

Through the native Tolq API, this operation is `GET /translations/requests/:id` (base URL `https://api.tolq.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-translation-request.md) for the provider-specific parameters and requirements.

