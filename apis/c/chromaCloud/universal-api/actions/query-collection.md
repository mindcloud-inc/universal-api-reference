# Chroma Cloud: Query collection

Queries a collection in Chroma Cloud.

```
GET https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/query-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chroma Cloud `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/query-collection?connectionId=$CONNECTION_ID&limit=25&offset=0&collectionId=string&queryEmbeddings%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "collectionId": "string",
  "queryEmbeddings[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/query-collection?${params}`, {
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
| `queryEmbeddings[]` | array<array> | yes | Query embedding vectors. |
| `nResults` | number | no |  |
| `include[]` | array<string> | no |  |
| `where` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "distances": [
        [
          "string"
        ]
      ],
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
      "include": [
        "string"
      ],
      "metadatas": [
        [
          "string"
        ]
      ],
      "uris": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `distances` | array<array> |  |
| `documents` | array<array> |  |
| `embeddings` | array<array> |  |
| `ids` | array<array> |  |
| `include` | array<string> |  |
| `metadatas` | array<array> |  |
| `uris` | array<array> |  |

## Native endpoint

Through the native Chroma Cloud API, this operation is `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/query` (base URL `https://api.trychroma.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/query-collection.md) for the provider-specific parameters and requirements.

