# LogMeIn: Update Draft Document

Updates an existing draft document in LogMeIn.

```
PUT https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/update-draft-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/update-draft-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "draftId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/update-draft-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "draftId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `draftId` | string | yes | Required draft ID. |
| `file` | file | no | PDF file replacement for file drafts. Mutually exclusive with content. |
| `title` | string | no | New title for the draft. |
| `content` | string | no | New Markdown content for text drafts. Mutually exclusive with file. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tenantIds` | string | no | Comma-separated tenant IDs for the draft. |
| `labels` | string | no | Comma-separated labels for the draft. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "id": "string",
      "lastModifiedAt": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "type": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `id` | string |  |
| `lastModifiedAt` | date |  |
| `title` | string |  |
| `type` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `PATCH /resolve/knowledge-base/v2/drafts/:draftId` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-draft-document.md) for the provider-specific parameters and requirements.

