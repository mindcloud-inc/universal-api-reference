# Wbiztool: Get Media File

Retrieves a specific media file from Wbiztool.

```
GET https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/get-media-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wbiztool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/get-media-file?connectionId=$CONNECTION_ID&mediaId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/get-media-file?${params}`, {
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
| `mediaId` | number | yes | Media file ID to fetch in the URL path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileExtension": "string",
      "fileName": "Ava Chen",
      "fileSize": 1,
      "fileSizeDisplay": "string",
      "fileType": "string",
      "fileUrl": "https://example.com",
      "id": 1,
      "isImage": true,
      "mimeType": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "originalFileName": "Ava Chen",
      "uploadedBy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `fileExtension` | string |  |
| `fileName` | string |  |
| `fileSize` | number |  |
| `fileSizeDisplay` | string |  |
| `fileType` | string |  |
| `fileUrl` | string |  |
| `id` | number |  |
| `isImage` | boolean |  |
| `mimeType` | string |  |
| `modifiedAt` | date |  |
| `originalFileName` | string |  |
| `uploadedBy` | string |  |

## Native endpoint

Through the native Wbiztool API, this operation is `POST /media/{{media_id}}/` (base URL `https://wbiztool.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-media-file.md) for the provider-specific parameters and requirements.

