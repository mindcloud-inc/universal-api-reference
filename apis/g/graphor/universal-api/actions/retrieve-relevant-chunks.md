# Graphor: Retrieve Relevant Chunks

Retrieves relevant document chunks from Graphor by semantic search.

```
GET https://connect.mindcloud.co/v1/universal/graphor/latest/actions/retrieve-relevant-chunks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Graphor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphor/latest/actions/retrieve-relevant-chunks?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphor/latest/actions/retrieve-relevant-chunks?${params}`, {
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
| `fileIds` | string | no | Optional list of file IDs to scope retrieval to specific documents. |
| `query` | string | yes | The semantic-search query used to retrieve relevant chunks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chunks": [
        {}
      ],
      "query": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chunks` | array<object> |  |
| `query` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Graphor API, this operation is `POST /prebuilt-rag` (base URL `https://sources.graphorlm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-relevant-chunks.md) for the provider-specific parameters and requirements.

