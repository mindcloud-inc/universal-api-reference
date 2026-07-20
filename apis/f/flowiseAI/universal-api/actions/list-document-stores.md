# FlowiseAI: List Document Stores

Retrieves all document stores from FlowiseAI.

```
GET https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/list-document-stores
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowiseAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/list-document-stores?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/list-document-stores?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native FlowiseAI API, this operation is `GET /document-store/store` (base URL `https://cloud.flowiseai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-document-stores.md) for the provider-specific parameters and requirements.

