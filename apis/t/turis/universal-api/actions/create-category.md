# Turis: Create Category

Creates a new category in Turis.

```
POST https://connect.mindcloud.co/v1/universal/turis/latest/actions/create-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Turis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/turis/latest/actions/create-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/turis/latest/actions/create-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category_custom_id` | string | no | Optional external category identifier. |
| `category_name` | string | no | Category name to create in Turis. |
| `parent_id` | string | no | Optional parent category ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryName": "Ava Chen",
      "categorySlug": "string",
      "id": 1,
      "isVisible": true,
      "parentId": 1,
      "position": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryName` | string |  |
| `categorySlug` | string |  |
| `id` | number |  |
| `isVisible` | boolean |  |
| `parentId` | number |  |
| `position` | number |  |

## Native endpoint

Through the native Turis API, this operation is `POST /api/public/v1/categories` (base URL `https://{{credentials.tenant}}.turis.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-category.md) for the provider-specific parameters and requirements.

