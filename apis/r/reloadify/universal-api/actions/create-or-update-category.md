# Reloadify: Create Or Update Category

Creates or updates a category in Reloadify.

```
PUT https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "language_id": "string",
  "category.id": "string",
  "category.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "language_id": "string",
    "category.id": "string",
    "category.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language_id` | string | yes | Language ID from the Reloadify language resource. |
| `category.id` | string | yes | Category identifier. |
| `category.name` | string | yes | Category name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": {},
      "id": "string",
      "name": "Ava Chen",
      "parentCategoryId": {},
      "updatedAt": {},
      "url": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | object |  |
| `id` | string |  |
| `name` | string |  |
| `parentCategoryId` | object |  |
| `updatedAt` | object |  |
| `url` | object |  |

## Native endpoint

Through the native Reloadify API, this operation is `PUT /v2/languages/:language_id/categories` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-category.md) for the provider-specific parameters and requirements.

