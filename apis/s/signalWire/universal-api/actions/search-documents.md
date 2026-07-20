# SignalWire: Search Documents

Searches documents in SignalWire by query string.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/search-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/search-documents?connectionId=$CONNECTION_ID&queryString=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "queryString": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/search-documents?${params}`, {
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
| `tags[]` | array<string> | no | Document tags. |
| `documentId` | string | no | Unique ID of a Document. |
| `queryString` | string | yes | Search term. |
| `distance` | number | no | Specifies how closely related the query is to the document. Low distance means high relevance and similarity. High distance means low relevance and similarity. |
| `count` | number | no | Specifies number of returned Chunks. |
| `language` | string | no | Language of the Document. |
| `posToExpand[]` | array<string> | no | Part of Speech considered for expansion or analysis. |
| `maxSynonyms` | number | no | Maximum number of synonyms to consider. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document_id": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document_id` | string | Unique ID of the Document. |
| `text` | string | A search result. |

## Native endpoint

Through the native SignalWire API, this operation is `POST /datasphere/documents/search` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-documents.md) for the provider-specific parameters and requirements.

