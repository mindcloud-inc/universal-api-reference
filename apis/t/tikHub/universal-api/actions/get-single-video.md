# TikHub: Get Single Video

Retrieves a TikTok video from TikHub.

```
GET https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-single-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-single-video?connectionId=$CONNECTION_ID&awemeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "awemeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-single-video?${params}`, {
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
| `awemeId` | string | yes | Video id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |

## Native endpoint

Through the native TikHub API, this operation is `GET /api/v1/tiktok/app/v3/fetch_one_video` (base URL `https://api.tikhub.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-single-video.md) for the provider-specific parameters and requirements.

