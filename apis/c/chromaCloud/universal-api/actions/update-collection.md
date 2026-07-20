# Chroma Cloud: Update collection

Updates a collection in Chroma Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/update-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chroma Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/update-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/update-collection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Collection UUID. |
| `newName` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `newMetadata` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chroma Cloud API returns.

## Native endpoint

Through the native Chroma Cloud API, this operation is `PUT /api/v2/tenants/:tenant/databases/:database/collections/:collection_id` (base URL `https://api.trychroma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-collection.md) for the provider-specific parameters and requirements.

