# Vectara: List Documents

Retrieves documents from a specific Vectara corpus.

```
GET https://connect.mindcloud.co/v1/universal/vectara/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/list-documents?connectionId=$CONNECTION_ID&corpusKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "corpusKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectara/latest/actions/list-documents?${params}`, {
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
| `corpusKey` | string | yes | Unique key of the corpus. |
| `limit` | number | no | Maximum number of documents to return. |
| `metadataFilter` | string | no | Metadata filter expression used to narrow listed documents. |
| `pageKey` | string | no | Cursor for the next page of documents. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        {}
      ],
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documents` | array<object> | List of documents. |
| `metadata` | object | Pagination metadata for the list response. |

## Native endpoint

Through the native Vectara API, this operation is `GET /v2/corpora/:corpus_key/documents` (base URL `https://api.vectara.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

