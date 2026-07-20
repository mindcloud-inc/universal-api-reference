# pixx.io: Download Files

Downloads converted files from your pixx.io workspace.

```
GET https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/download-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pixx.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/download-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/download-files?${params}`, {
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
| `fileName` | string | no | Output file name. |
| `ids` | number<number> | no | File IDs to convert or download. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobID": 1,
      "omittedFiles": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobID` | number |  |
| `omittedFiles` | array<object> |  |
| `success` | boolean |  |

## Native endpoint

Through the native pixx.io API, this operation is `GET /files/convert` (base URL `https://mindcloudpixx260413.px.media/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-files.md) for the provider-specific parameters and requirements.

