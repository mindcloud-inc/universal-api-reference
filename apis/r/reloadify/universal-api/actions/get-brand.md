# Reloadify: Get Brand

Retrieves a brand from Reloadify.

```
GET https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-brand
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-brand?connectionId=$CONNECTION_ID&languageId=string&brandId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "languageId": "string",
  "brandId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-brand?${params}`, {
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
| `languageId` | string | yes | Reloadify language ID. |
| `brandId` | string | yes | Brand identifier. |

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

Through the native Reloadify API, this operation is `GET /v2/languages/:language_id/brands/:brand_id` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-brand.md) for the provider-specific parameters and requirements.

