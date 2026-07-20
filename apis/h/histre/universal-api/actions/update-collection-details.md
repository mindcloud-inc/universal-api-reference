# Histre: Update Collection Details

Updates collection details in Histre.

```
PUT https://connect.mindcloud.co/v1/universal/histre/latest/actions/update-collection-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Histre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/histre/latest/actions/update-collection-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/histre/latest/actions/update-collection-details', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookId` | string | yes | Identifier of the Histre collection to update. |
| `title` | string | no | Optional new title for the collection. |
| `description` | string | no | Optional new description for the collection. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Histre API returns.

## Native endpoint

Through the native Histre API, this operation is `PATCH /api/v1/collections/[:book_id]/` (base URL `https://histre.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-collection-details.md) for the provider-specific parameters and requirements.

