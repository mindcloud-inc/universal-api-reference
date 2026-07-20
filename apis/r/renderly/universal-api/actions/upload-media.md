# Renderly: Upload Media

Creates a media upload URL in Renderly.

```
POST https://connect.mindcloud.co/v1/universal/renderly/latest/actions/upload-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Renderly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/renderly/latest/actions/upload-media" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contentType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/renderly/latest/actions/upload-media', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contentType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contentType` | string | yes | MIME type of the file to upload, for example video/mp4 or image/png. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "fileUrl": "https://example.com",
      "id": "string",
      "uploadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresAt` | date |  |
| `fileUrl` | string |  |
| `id` | string |  |
| `uploadUrl` | string |  |

## Native endpoint

Through the native Renderly API, this operation is `POST /uploads` (base URL `https://renderly.video/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-media.md) for the provider-specific parameters and requirements.

