# Docutray: Sync Knowledge Base



```
POST https://connect.mindcloud.co/v1/universal/docutray/latest/actions/sync-knowledge-base
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docutray `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docutray/latest/actions/sync-knowledge-base" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docutray/latest/actions/sync-knowledge-base', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique ID of the Knowledge Base |
| `force` | boolean | no | Force regeneration of all embeddings |
| `regenerateEmbeddings` | boolean | no | Regenerate existing embeddings |
| `syncExternalSources` | boolean | no | Sync with configured external sources |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "2026-05-07T12:00:00.000Z",
      "documentsProcessed": 1,
      "embeddingsGenerated": 1,
      "errors": [
        {}
      ],
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "syncId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | date |  |
| `documentsProcessed` | number |  |
| `embeddingsGenerated` | number |  |
| `errors` | array<object> |  |
| `startedAt` | date |  |
| `status` | string |  |
| `syncId` | string |  |

## Native endpoint

Through the native Docutray API, this operation is `POST api/knowledge-bases/:id/sync` (base URL `https://app.docutray.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sync-knowledge-base.md) for the provider-specific parameters and requirements.

