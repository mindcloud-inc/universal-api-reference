# Dropbox: Get File Request

Retrieves a file request from Dropbox.

```
GET https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-file-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-file-request?connectionId=$CONNECTION_ID&id=id%3A3m0pssQd5QkAAAAAAAAAHQ" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "id:3m0pssQd5QkAAAAAAAAAHQ"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-file-request?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the file request to retrieve. Example: `id:3m0pssQd5QkAAAAAAAAAHQ`. |

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

Through the native Dropbox API, this operation is `POST /file_requests/get` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-request.md) for the provider-specific parameters and requirements.

