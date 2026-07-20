# pixx.io: Download File

Downloads a converted file from your pixx.io workspace.

```
GET https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/download-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pixx.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/download-file?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/download-file?${params}`, {
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
| `downloadFormatId` | number | no | Download format ID when downloadType is downloadFormat. |
| `downloadType` | string | no | Download type such as original, preview, custom, or downloadFormat. |
| `fileExtension` | string | no | Output file extension for custom conversion. |
| `height` | number | no | Requested output height for custom conversion. |
| `id` | number | yes | The pixx.io file ID to download or convert. |
| `width` | number | no | Requested output width for custom conversion. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "directLinkID": 1,
      "downloadURL": "https://example.com",
      "fileExtension": "string",
      "fileName": "Ava Chen",
      "fileSize": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `directLinkID` | number |  |
| `downloadURL` | string |  |
| `fileExtension` | string |  |
| `fileName` | string |  |
| `fileSize` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native pixx.io API, this operation is `GET /files/:id/convert` (base URL `https://mindcloudpixx260413.px.media/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-file.md) for the provider-specific parameters and requirements.

