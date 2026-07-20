# VdoCipher: Replace Video Upload Policy

Retrieves an upload policy for replacing a VdoCipher video.

```
GET https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/replace-video-upload-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VdoCipher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/replace-video-upload-policy?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/replace-video-upload-policy?${params}`, {
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
| `videoId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "policy": "string",
      "uploadLink": "https://example.com",
      "x-amz-algorithm": "string",
      "x-amz-credentials": "string",
      "x-amz-date": "string",
      "x-amz-signature": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |
| `policy` | string |  |
| `uploadLink` | string |  |
| `x-amz-algorithm` | string |  |
| `x-amz-credentials` | string |  |
| `x-amz-date` | string |  |
| `x-amz-signature` | string |  |

## Native endpoint

Through the native VdoCipher API, this operation is `PUT /videos/:videoId` (base URL `https://dev.vdocipher.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-video-upload-policy.md) for the provider-specific parameters and requirements.

