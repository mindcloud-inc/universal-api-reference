# Tettra: Create Category

Creates a new category in Tettra.

```
POST https://connect.mindcloud.co/v1/universal/tettra/latest/actions/create-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tettra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tettra/latest/actions/create-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tettra/latest/actions/create-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Category description. |
| `name` | string | yes | Category name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": {
        "color": "string",
        "description": "string",
        "icon": "string",
        "id": 1,
        "name": "Ava Chen",
        "visibility": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category.color` | string |  |
| `category.description` | string |  |
| `category.icon` | string |  |
| `category.id` | number |  |
| `category.name` | string |  |
| `category.visibility` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Tettra API, this operation is `POST /teams/85329/categories` (base URL `https://app.tettra.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-category.md) for the provider-specific parameters and requirements.

