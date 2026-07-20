# Dropbox: Create File Request

Creates a file request in Dropbox.

```
POST https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/create-file-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/create-file-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "Upload tax documents",
  "destination": "/Codex Dropbox Fixtures/File Requests"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/create-file-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "Upload tax documents",
    "destination": "/Codex Dropbox Fixtures/File Requests"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Title shown on the file request page. Example: `Upload tax documents`. |
| `destination` | string | yes | Dropbox folder path where uploaded files should be stored. Example: `/Codex Dropbox Fixtures/File Requests`. |
| `open` | boolean | no | Whether the file request should be open after creation. Example: `true`. |
| `description` | string | no | Optional description shown to request participants. Example: `Please upload the requested files here.`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deadline.value` | string | no | Deadline for the file request in RFC 3339 format. Example: `2026-03-20T23:59:00Z`. |
| `deadline.allowLateUploads` | boolean | no | Allow uploads after the deadline passes. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "destination": "string",
      "fileCount": 1,
      "id": "string",
      "isOpen": true,
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `description` | string |  |
| `destination` | string |  |
| `fileCount` | number |  |
| `id` | string |  |
| `isOpen` | boolean |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Dropbox API, this operation is `POST /file_requests/create` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-file-request.md) for the provider-specific parameters and requirements.

