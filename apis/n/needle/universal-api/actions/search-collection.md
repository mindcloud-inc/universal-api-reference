# Needle: Search Collection

Searches a collection in Needle by query.

```
GET https://connect.mindcloud.co/v1/universal/needle/latest/actions/search-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Needle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/needle/latest/actions/search-collection?connectionId=$CONNECTION_ID&collectionId=string&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string",
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/needle/latest/actions/search-collection?${params}`, {
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
| `collectionId` | string | yes | ID of the collection to search |
| `text` | string | yes | Search text to query in the collection |
| `topK` | number | no | Maximum number of search results to return |
| `offset` | number | no | Offset to start returning search results from |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "distance": 1,
      "fileId": "string",
      "id": "string",
      "index": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `distance` | number |  |
| `fileId` | string |  |
| `id` | string |  |
| `index` | number |  |

## Native endpoint

Through the native Needle API, this operation is `POST https://search.needle.app/api/v1/collections/:collectionId/search` (base URL `https://needle.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-collection.md) for the provider-specific parameters and requirements.

