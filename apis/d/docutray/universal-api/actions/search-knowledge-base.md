# Docutray: Advanced Search Knowledge Base



```
GET https://connect.mindcloud.co/v1/universal/docutray/latest/actions/search-knowledge-base
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docutray `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docutray/latest/actions/search-knowledge-base?connectionId=$CONNECTION_ID&id=string&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docutray/latest/actions/search-knowledge-base?${params}`, {
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
| `id` | string | yes | Unique ID of the Knowledge Base |
| `query` | string | yes | Search query |
| `limit` | number | no | Maximum number of results |
| `similarityThreshold` | number | no | Minimum similarity threshold |
| `includeMetadata` | boolean | no | Include metadata in results |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document": {},
      "similarity": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document` | object |  |
| `similarity` | number |  |

## Native endpoint

Through the native Docutray API, this operation is `POST api/knowledge-bases/:id/search` (base URL `https://app.docutray.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-knowledge-base.md) for the provider-specific parameters and requirements.

