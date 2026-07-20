# HappyScribe: Get Signed URL

Retrieves a signed upload URL from HappyScribe.

```
GET https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/get-signed-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyScribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/get-signed-url?connectionId=$CONNECTION_ID&filename=my_media.mp3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filename": "my_media.mp3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/get-signed-url?${params}`, {
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
| `filename` | string | yes | Filename and extension of the media file to upload, for example my_media.mp3. Example: `my_media.mp3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "signedUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `signedUrl` | string | Pre-signed S3 URL to upload the media file to HappyScribe storage. |

## Native endpoint

Through the native HappyScribe API, this operation is `GET /uploads/new` (base URL `https://www.happyscribe.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signed-url.md) for the provider-specific parameters and requirements.

