# TikHub: Get Video Comments

Retrieves comments for a TikTok video from TikHub.

```
GET https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-video-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-video-comments?connectionId=$CONNECTION_ID&awemeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "awemeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-video-comments?${params}`, {
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
| `cursor` | number | no | Cursor |
| `count` | number | no | Number |

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

Through the native TikHub API, this operation is `GET /api/v1/tiktok/app/v3/fetch_video_comments` (base URL `https://api.tikhub.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-comments.md) for the provider-specific parameters and requirements.

