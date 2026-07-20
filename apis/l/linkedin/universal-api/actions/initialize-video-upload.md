# LinkedIn: Initialize Video Upload

Initializes a video upload in LinkedIn.

```
POST https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/initialize-video-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/initialize-video-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "initializeUploadRequest.owner": "urn:li:person:vdyhqnicOV",
  "initializeUploadRequest.fileSizeBytes": "1200345"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/initialize-video-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "initializeUploadRequest.owner": "urn:li:person:vdyhqnicOV",
    "initializeUploadRequest.fileSizeBytes": "1200345"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `initializeUploadRequest.owner` | string | yes | Owner URN for the member initializing the upload. Example: `urn:li:person:vdyhqnicOV`. |
| `initializeUploadRequest.fileSizeBytes` | number | yes | Example: `1200345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {
        "uploadInstructions": [
          {
            "firstByte": 1,
            "lastByte": 1,
            "uploadUrl": "https://example.com"
          }
        ],
        "uploadToken": "string",
        "uploadUrlsExpireAt": 1,
        "video": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value.uploadInstructions[].firstByte` | number |  |
| `value.uploadInstructions[].lastByte` | number |  |
| `value.uploadInstructions[].uploadUrl` | string |  |
| `value.uploadToken` | string |  |
| `value.uploadUrlsExpireAt` | number |  |
| `value.video` | string |  |

## Native endpoint

Through the native LinkedIn API, this operation is `POST /rest/videos?action=initializeUpload` (base URL `https://api.linkedin.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initialize-video-upload.md) for the provider-specific parameters and requirements.

