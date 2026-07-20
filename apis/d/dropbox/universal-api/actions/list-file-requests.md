# Dropbox: List File Requests

Retrieves file requests for the current user from Dropbox.

```
GET https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/list-file-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/list-file-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/list-file-requests?${params}`, {
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
| `limit` | number | no | Maximum number of file requests to return. Example: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "fileRequests": [
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
      "hasMore": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string |  |
| `fileRequests[].created` | date |  |
| `fileRequests[].description` | string |  |
| `fileRequests[].destination` | string |  |
| `fileRequests[].fileCount` | number |  |
| `fileRequests[].id` | string |  |
| `fileRequests[].isOpen` | boolean |  |
| `fileRequests[].title` | string |  |
| `fileRequests[].url` | string |  |
| `hasMore` | boolean |  |

## Native endpoint

Through the native Dropbox API, this operation is `POST /file_requests/list_v2` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-file-requests.md) for the provider-specific parameters and requirements.

