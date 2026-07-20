# Dropbox: Update File Request

Updates an existing file request in Dropbox.

```
PUT https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/update-file-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/update-file-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "id:3m0pssQd5QkAAAAAAAAAHQ"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/update-file-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "id:3m0pssQd5QkAAAAAAAAAHQ"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the file request to update. Example: `id:3m0pssQd5QkAAAAAAAAAHQ`. |
| `title` | string | no | Updated title for the file request. Example: `Updated upload request`. |
| `destination` | string | no | Updated Dropbox folder path for uploaded files. Example: `/Codex Dropbox Fixtures/File Requests`. |
| `open` | boolean | no | Whether the file request should remain open. Example: `false`. |
| `description` | string | no | Updated description shown to request participants. Example: `Closing the request after verification.`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deadline.value` | string | no | Updated deadline in RFC 3339 format. Example: `2026-03-21T23:59:00Z`. |
| `deadline.allowLateUploads` | boolean | no | Allow uploads after the updated deadline passes. Example: `false`. |

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

Through the native Dropbox API, this operation is `POST /file_requests/update` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-file-request.md) for the provider-specific parameters and requirements.

