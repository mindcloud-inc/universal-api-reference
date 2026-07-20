# Chroma Cloud: Get records

Retrieves records from a collection in Chroma Cloud.

```
GET https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/get-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chroma Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/get-records?connectionId=$CONNECTION_ID&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/get-records?${params}`, {
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
| `ids[]` | array<string> | no |  |
| `where` | object | no |  |
| `include[]` | array<string> | no | Fields to include in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        "string"
      ],
      "embeddings": [
        [
          "string"
        ]
      ],
      "ids": [
        "string"
      ],
      "include": [
        "string"
      ],
      "metadatas": [
        {}
      ],
      "uris": [
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
| `documents` | array<string> |  |
| `embeddings` | array<array> |  |
| `ids` | array<string> |  |
| `include` | array<string> |  |
| `metadatas` | array<object> |  |
| `uris` | array<string> |  |

## Native endpoint

Through the native Chroma Cloud API, this operation is `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/get` (base URL `https://api.trychroma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-records.md) for the provider-specific parameters and requirements.

