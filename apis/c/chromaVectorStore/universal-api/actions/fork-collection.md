# Chroma Vector Store: Fork Collection

Creates a fork of an existing collection in Chroma.

```
POST https://connect.mindcloud.co/v1/universal/chromaVectorStore/latest/actions/fork-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chroma Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chromaVectorStore/latest/actions/fork-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "database": "string",
  "newName": "Ava Chen",
  "tenant": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chromaVectorStore/latest/actions/fork-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "database": "string",
    "newName": "Ava Chen",
    "tenant": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Collection UUID |
| `database` | string | yes | Database name |
| `newName` | string | yes | Name for the forked collection |
| `tenant` | string | yes | Tenant UUID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configuration_json": {},
      "database": "string",
      "dimension": 1,
      "id": "string",
      "log_position": 1,
      "metadata": {},
      "name": "Ava Chen",
      "schema": {},
      "tenant": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configuration_json` | object |  |
| `database` | string |  |
| `dimension` | number |  |
| `id` | string |  |
| `log_position` | number |  |
| `metadata` | object |  |
| `name` | string |  |
| `schema` | object |  |
| `tenant` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Chroma Vector Store API, this operation is `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/fork` (base URL `https://api.trychroma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fork-collection.md) for the provider-specific parameters and requirements.

