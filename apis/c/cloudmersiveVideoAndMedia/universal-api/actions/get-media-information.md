# Cloudmersive Video and Media: Get Media Information

Retrieves media information from Cloudmersive Video and Media.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveVideoAndMedia/latest/actions/get-media-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Video and Media `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveVideoAndMedia/latest/actions/get-media-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveVideoAndMedia/latest/actions/get-media-information?${params}`, {
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
| `fileUrl` | string | no | URL of a video or audio file to inspect. |
| `inputFile` | file | no | Input video or audio file to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BitRate": 1,
      "Duration": 1,
      "FileFormat": "string",
      "FileFormatFull": "string",
      "Height": 1,
      "Size": 1,
      "StartTime": 1,
      "Successful": true,
      "ValidFileFormats": [
        "string"
      ],
      "Width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BitRate` | number | Media bit rate. |
| `Duration` | number | Media duration in seconds. |
| `FileFormat` | string | Short media format name. |
| `FileFormatFull` | string | Full media format name. |
| `Height` | number | Video height when the file is a video. |
| `Size` | number | File size in bytes. |
| `StartTime` | number | Media start time. |
| `Successful` | boolean | True if the operation was successful. |
| `ValidFileFormats` | array<string> | Valid detected formats. |
| `Width` | number | Video width when the file is a video. |

## Native endpoint

Through the native Cloudmersive Video and Media API, this operation is `POST /video/convert/get-info` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-media-information.md) for the provider-specific parameters and requirements.

