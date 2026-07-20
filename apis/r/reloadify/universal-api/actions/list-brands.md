# Reloadify: List Brands

Retrieves brands from Reloadify.

```
GET https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-brands
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-brands?connectionId=$CONNECTION_ID&limit=25&offset=0&languageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "languageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-brands?${params}`, {
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
| `created_after` | string | no | Only include brands created after this timestamp. |
| `created_before` | string | no | Only include brands created before this timestamp. |
| `languageId` | string | yes | Reloadify language ID. |
| `updated_after` | string | no | Only include brands updated after this timestamp. |
| `updated_before` | string | no | Only include brands updated before this timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "created_at": "string",
      "custom_attributes": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "product_ids": [
        "string"
      ],
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
| `content` | string |  |
| `created_at` | string |  |
| `custom_attributes` | array<object> |  |
| `id` | string |  |
| `name` | string |  |
| `product_ids` | array<string> |  |
| `updated_at` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Reloadify API, this operation is `GET /v2/languages/:language_id/brands` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-brands.md) for the provider-specific parameters and requirements.

