# PocketSmith: Update Category

Updates a PocketSmith category.

```
PUT https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/update-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PocketSmith `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/update-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "categoryId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/update-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "categoryId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categoryId` | number | yes | The unique identifier of the PocketSmith category. |
| `colour` | string | no | A new CSS-style hex colour for the category. |
| `title` | string | no | A new title for the category. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PocketSmith API returns.

## Native endpoint

Through the native PocketSmith API, this operation is `PUT /categories/:id` (base URL `https://api.pocketsmith.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-category.md) for the provider-specific parameters and requirements.

