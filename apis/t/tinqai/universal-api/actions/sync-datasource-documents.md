# Tinq.ai: Sync Datasource Documents



```
PUT https://connect.mindcloud.co/v1/universal/tinqai/latest/actions/sync-datasource-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tinqai/latest/actions/sync-datasource-documents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasource": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tinqai/latest/actions/sync-datasource-documents', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasource": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasource` | string | yes | Datasource ID to sync. |
| `documents[]` | array<string> | no | Optional document slugs to sync; omit to let Tinq decide changed documents. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Tinq.ai API returns.

## Native endpoint

Through the native Tinq.ai API, this operation is `POST /api/v2/datasources/sync/:workspaceId` (base URL `https://tinq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sync-datasource-documents.md) for the provider-specific parameters and requirements.

