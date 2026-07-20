# Nuclino: Update item or collection

Updates an existing item or collection in Nuclino.

```
PUT https://connect.mindcloud.co/v1/universal/nuclino/latest/actions/update-item-or-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nuclino `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nuclino/latest/actions/update-item-or-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nuclino/latest/actions/update-item-or-collection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | no |  |
| `id` | string | yes |  |
| `title` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nuclino API returns.

## Native endpoint

Through the native Nuclino API, this operation is `PUT /items/:id` (base URL `https://api.nuclino.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item-or-collection.md) for the provider-specific parameters and requirements.

