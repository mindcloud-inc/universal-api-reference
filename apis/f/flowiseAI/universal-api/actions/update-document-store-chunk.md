# FlowiseAI: Update Document Store Chunk

Updates a specific document chunk in FlowiseAI.

```
PUT https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/update-document-store-chunk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowiseAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/update-document-store-chunk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chunkId": "string",
  "loaderId": "string",
  "storeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/update-document-store-chunk', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chunkId": "string",
    "loaderId": "string",
    "storeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | no | JSON body with documented chunk fields to update. |
| `chunkId` | string | yes | Document store chunk ID. |
| `loaderId` | string | yes | Document loader ID containing the chunk. |
| `storeId` | string | yes | Document store ID containing the chunk. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chunks": [
        {}
      ],
      "count": 1,
      "currentPage": 1,
      "description": "string",
      "file": {},
      "storeName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chunks` | array<object> |  |
| `count` | number |  |
| `currentPage` | number |  |
| `description` | string |  |
| `file` | object |  |
| `storeName` | string |  |

## Native endpoint

Through the native FlowiseAI API, this operation is `PUT /document-store/chunks/{storeId}/{loaderId}/{chunkId}` (base URL `https://cloud.flowiseai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document-store-chunk.md) for the provider-specific parameters and requirements.

