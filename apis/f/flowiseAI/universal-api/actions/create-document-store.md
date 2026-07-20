# FlowiseAI: Create Document Store

Creates a new document store in FlowiseAI.

```
POST https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/create-document-store
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowiseAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/create-document-store" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/create-document-store', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | no | JSON body with documented document store fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDate": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "embeddingConfig": "string",
      "id": "string",
      "loaders": "string",
      "name": "Ava Chen",
      "recordManagerConfig": "string",
      "status": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z",
      "vectorStoreConfig": "string",
      "whereUsed": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDate` | date |  |
| `description` | string |  |
| `embeddingConfig` | string |  |
| `id` | string |  |
| `loaders` | string |  |
| `name` | string |  |
| `recordManagerConfig` | string |  |
| `status` | string |  |
| `updatedDate` | date |  |
| `vectorStoreConfig` | string |  |
| `whereUsed` | string |  |

## Native endpoint

Through the native FlowiseAI API, this operation is `POST /document-store/store` (base URL `https://cloud.flowiseai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document-store.md) for the provider-specific parameters and requirements.

