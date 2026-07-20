# Chroma Cloud: Fork collection

Creates a fork of a collection in Chroma Cloud.

```
POST https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/fork-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chroma Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/fork-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "newName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/fork-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "newName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Collection UUID. |
| `newName` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "database": "string",
      "dimension": 1,
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
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
| `database` | string |  |
| `dimension` | number |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `tenant` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Chroma Cloud API, this operation is `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/fork` (base URL `https://api.trychroma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fork-collection.md) for the provider-specific parameters and requirements.

