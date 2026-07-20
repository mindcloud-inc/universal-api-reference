# Reloadify: Create Or Update Brand

Creates or updates a brand in Reloadify.

```
PUT https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-brand
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-brand" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "languageId": "string",
  "brand.id": "string",
  "brand.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-brand', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "languageId": "string",
    "brand.id": "string",
    "brand.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageId` | string | yes | Reloadify language ID. |
| `brand.id` | string | yes | Brand identifier. |
| `brand.name` | string | yes | Brand name. |

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

Through the native Reloadify API, this operation is `PUT /v2/languages/:language_id/brands` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-brand.md) for the provider-specific parameters and requirements.

