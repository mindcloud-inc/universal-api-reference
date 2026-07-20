# Dust: Upsert Document



```
POST https://connect.mindcloud.co/v1/universal/dust/latest/actions/upsert-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dust `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dust/latest/actions/upsert-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataSourceId": "string",
  "document_id": "string",
  "spaceId": "string",
  "text": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dust/latest/actions/upsert-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataSourceId": "string",
    "document_id": "string",
    "spaceId": "string",
    "text": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataSourceId` | string | yes | Dust data source sId. |
| `document_id` | string | yes | Stable external ID for the document. |
| `spaceId` | string | yes | Dust space sId. |
| `text` | string | yes | Plain text document content. |
| `title` | string | yes | Document title. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dust API returns.

## Native endpoint

Through the native Dust API, this operation is `POST /api/v1/w/:workspaceId/spaces/:spaceId/data_sources/:dataSourceId/documents` (base URL `https://dust.tt`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-document.md) for the provider-specific parameters and requirements.

