# LogMeIn: Create Document

Creates a new knowledge base document in LogMeIn.

```
POST https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Required document title. |
| `file` | file | no | PDF file for file documents. Mutually exclusive with content. |
| `content` | string | no | Markdown content for text documents. Mutually exclusive with file. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tenantIds` | string | no | Comma-separated tenant IDs for the document. |
| `labels` | string | no | Comma-separated labels for the document. |
| `visibility` | string | no | Document visibility. |
| `folderId` | string | no | Folder ID to place the document in. |

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

Through the native LogMeIn API, this operation is `POST /resolve/knowledge-base/v2/documents` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

