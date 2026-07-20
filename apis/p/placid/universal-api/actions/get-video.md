# Placid: Get Video

Retrieves a video render from Placid.

```
GET https://connect.mindcloud.co/v1/universal/placid/latest/actions/get-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placid/latest/actions/get-video?connectionId=$CONNECTION_ID&videoId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placid/latest/actions/get-video?${params}`, {
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
| `videoId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "passthrough": "string",
      "pollingUrl": "https://example.com",
      "srtFiles": [
        {}
      ],
      "status": "string",
      "statusDisplay": "string",
      "transferUrl": "https://example.com",
      "type": "string",
      "videoUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `passthrough` | string |  |
| `pollingUrl` | string |  |
| `srtFiles` | array<object> |  |
| `status` | string |  |
| `statusDisplay` | string |  |
| `transferUrl` | string |  |
| `type` | string |  |
| `videoUrl` | string |  |

## Native endpoint

Through the native Placid API, this operation is `GET /api/rest/videos/:videoId` (base URL `https://api.placid.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video.md) for the provider-specific parameters and requirements.

