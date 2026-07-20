# VdoCipher: Get Video

Retrieves video details from VdoCipher.

```
GET https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/get-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VdoCipher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/get-video?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/get-video?${params}`, {
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
      "description": "string",
      "id": "string",
      "length": 1,
      "mobileReso": [
        1
      ],
      "public": true,
      "reso": [
        1
      ],
      "status": "string",
      "thumbUrl": "https://example.com",
      "title": "string",
      "upload_time": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `length` | number |  |
| `mobileReso` | array<number> |  |
| `public` | boolean |  |
| `reso` | array<number> |  |
| `status` | string |  |
| `thumbUrl` | string |  |
| `title` | string |  |
| `upload_time` | number |  |

## Native endpoint

Through the native VdoCipher API, this operation is `GET /videos/:videoId` (base URL `https://dev.vdocipher.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video.md) for the provider-specific parameters and requirements.

