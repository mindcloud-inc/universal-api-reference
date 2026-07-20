# LogMeIn: Create Draft Document

Creates a new draft document in LogMeIn.

```
POST https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/create-draft-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/create-draft-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/create-draft-document', {
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
| `documentId` | string | no | Existing document ID to create a draft for. Omit to create a standalone draft. |
| `file` | file | no | PDF file for file drafts. Mutually exclusive with content. |
| `title` | string | no | Draft title. Required when documentId is omitted. |
| `content` | string | no | Markdown content for text drafts. Mutually exclusive with file. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tenantIds` | string | no | Comma-separated tenant IDs for the draft. |
| `labels` | string | no | Comma-separated labels for the draft. |
| `visibility` | string | no | Draft visibility. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `id` | string |  |
| `lastModifiedAt` | date |  |
| `title` | string |  |
| `type` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `POST /resolve/knowledge-base/v2/drafts` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-draft-document.md) for the provider-specific parameters and requirements.

