# VdoCipher: Create Video OTP

Creates a playback OTP in VdoCipher.

```
POST https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/create-video-otp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VdoCipher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/create-video-otp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/create-video-otp', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `annotate` | string | no |  |
| `forcedBitrate` | number | no |  |
| `ipGeoRules` | string | no |  |
| `nocdn` | string | no |  |
| `ttl` | number | no |  |
| `videoId` | string | no |  |
| `whitelisthref` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "otp": "string",
      "playbackInfo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `otp` | string |  |
| `playbackInfo` | string |  |

## Native endpoint

Through the native VdoCipher API, this operation is `POST /videos/:videoId/otp` (base URL `https://dev.vdocipher.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-video-otp.md) for the provider-specific parameters and requirements.

