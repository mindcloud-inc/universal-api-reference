# BlogIn: Update Category

Updates an existing category in BlogIn.

```
PUT https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/update-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlogIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/update-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/update-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The ID of the category to update. |
| `name` | string | yes | The name of the category. |
| `position` | number | no | The position of the category. |
| `locked` | boolean | no | Whether the category is locked. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "locked": true,
      "name": "Ava Chen",
      "parent": 1,
      "position": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `locked` | boolean |  |
| `name` | string |  |
| `parent` | number |  |
| `position` | number |  |

## Native endpoint

Through the native BlogIn API, this operation is `POST /categories/:id` (base URL `https://blogin.co/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-category.md) for the provider-specific parameters and requirements.

