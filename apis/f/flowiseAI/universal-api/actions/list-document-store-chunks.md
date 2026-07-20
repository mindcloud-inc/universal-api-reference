# FlowiseAI: List Document Store Chunks

Retrieves chunks from a FlowiseAI document loader.

```
GET https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/list-document-store-chunks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowiseAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/list-document-store-chunks?connectionId=$CONNECTION_ID&loaderId=string&pageNo=1&storeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "loaderId": "string",
  "pageNo": "1",
  "storeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/list-document-store-chunks?${params}`, {
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
| `loaderId` | string | yes | Document loader ID within the document store. |
| `pageNo` | number | yes | Pagination number for document store chunks. |
| `storeId` | string | yes | Document store ID for chunk listing. |

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

Through the native FlowiseAI API, this operation is `GET /document-store/chunks/{storeId}/{loaderId}/{pageNo}` (base URL `https://cloud.flowiseai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-document-store-chunks.md) for the provider-specific parameters and requirements.

