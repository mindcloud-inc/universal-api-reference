# DocsBot AI: Retry Source Indexing

Updates a source to retry indexing in DocsBot AI.

```
PUT https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/retry-source-indexing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocsBot AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/retry-source-indexing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": "string",
  "sourceId": "string",
  "teamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/retry-source-indexing', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": "string",
    "sourceId": "string",
    "teamId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | string | yes | The DocsBot bot ID. |
| `sourceId` | string | yes | The DocsBot source ID. |
| `teamId` | string | yes | The DocsBot team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chunkCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "file": "string",
      "id": "string",
      "pageCount": 1,
      "status": "string",
      "title": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chunkCount` | number |  |
| `createdAt` | date |  |
| `file` | string |  |
| `id` | string |  |
| `pageCount` | number |  |
| `status` | string |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native DocsBot AI API, this operation is `PUT /teams/:teamId/bots/:botId/sources/:sourceId` (base URL `https://docsbot.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retry-source-indexing.md) for the provider-specific parameters and requirements.

