# Chroma Cloud: Add records

Adds records to a collection in Chroma Cloud.

```
POST https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/add-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chroma Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/add-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "ids[]": [
    "string"
  ],
  "embeddings[]": [
    [
      "string"
    ]
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/add-records', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "ids[]": ["string"],
    "embeddings[]": [["string"]]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Collection UUID. |
| `ids[]` | array<string> | yes | Unique identifiers for each record. |
| `embeddings[]` | array<array> | yes | Embedding vectors corresponding to the record IDs. |
| `documents[]` | array<string> | no |  |
| `metadatas[]` | array<object> | no |  |
| `uris[]` | array<string> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chroma Cloud API returns.

## Native endpoint

Through the native Chroma Cloud API, this operation is `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/add` (base URL `https://api.trychroma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-records.md) for the provider-specific parameters and requirements.

