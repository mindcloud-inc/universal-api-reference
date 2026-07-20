# Hippo Video: Get Transcoded Video Download URL

Retrieves a download URL for a transcoded Hippo Video archive.

```
GET https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/get-transcoded-video-download-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hippo Video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/get-transcoded-video-download-url?connectionId=$CONNECTION_ID&videoToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/get-transcoded-video-download-url?${params}`, {
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
| `videoToken` | string | yes | Unique video token |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Hippo Video API, this operation is `POST /video/transcoded/signed_url` (base URL `https://www.hippovideo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transcoded-video-download-url.md) for the provider-specific parameters and requirements.

