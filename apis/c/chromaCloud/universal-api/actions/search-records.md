# Chroma Cloud: Search records

Searches records in a collection in Chroma Cloud.

```
GET https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/search-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chroma Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/search-records?connectionId=$CONNECTION_ID&collectionId=string&searches%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string",
  "searches[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/search-records?${params}`, {
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
| `collectionId` | string | yes | Collection UUID. |
| `searches[]` | array<object> | yes | Array of Search API search payloads. |
| `readLevel` | string | no | Read level for consistency vs performance. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        [
          "string"
        ]
      ],
      "embeddings": [
        [
          "string"
        ]
      ],
      "ids": [
        [
          "string"
        ]
      ],
      "metadatas": [
        [
          "string"
        ]
      ],
      "scores": [
        [
          "string"
        ]
      ],
      "select": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documents` | array<array> |  |
| `embeddings` | array<array> |  |
| `ids` | array<array> |  |
| `metadatas` | array<array> |  |
| `scores` | array<array> |  |
| `select` | array<string> |  |

## Native endpoint

Through the native Chroma Cloud API, this operation is `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/search` (base URL `https://api.trychroma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-records.md) for the provider-specific parameters and requirements.

