# ChipBot: Get Video



```
GET https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/get-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChipBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/get-video?connectionId=$CONNECTION_ID&videoExpId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoExpId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/get-video?${params}`, {
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
| `videoExpId` | string | yes | The video experience identifier, for example videxp_xxx. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "buttons": [
        {}
      ],
      "domainId": "string",
      "id": "string",
      "state": "string",
      "type": "string",
      "videoDurationSeconds": 1,
      "videoLocalSrc": "string",
      "videoPosterSrc": "string",
      "videoSrc": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | Owning account identifier. |
| `buttons` | array<object> | Configured action buttons. |
| `domainId` | string | Owning domain identifier. |
| `id` | string | Video experience identifier. |
| `state` | string | Video experience state. |
| `type` | string | Video experience type. |
| `videoDurationSeconds` | number | Video duration in seconds. |
| `videoLocalSrc` | string | Local video source path. |
| `videoPosterSrc` | string | Poster image path. |
| `videoSrc` | string | Primary video source path. |

## Native endpoint

Through the native ChipBot API, this operation is `GET /api/v2/connect/accounts/:accountId/domains/:domainId/video-exp/:videoExpId` (base URL `https://getchipbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video.md) for the provider-specific parameters and requirements.

