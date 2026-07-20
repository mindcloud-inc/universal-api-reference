# Instructure: Get File

Retrieves a file from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-file?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-file?${params}`, {
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
| `fileId` | string | yes | The Canvas file ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "createdAt": "string",
      "displayName": "Ava Chen",
      "filename": "Ava Chen",
      "folderId": 1,
      "hidden": true,
      "id": 1,
      "locked": true,
      "size": 1,
      "thumbnailUrl": "https://example.com",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `createdAt` | string |  |
| `displayName` | string |  |
| `filename` | string |  |
| `folderId` | number |  |
| `hidden` | boolean |  |
| `id` | number |  |
| `locked` | boolean |  |
| `size` | number |  |
| `thumbnailUrl` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `GET /files/:file_id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

