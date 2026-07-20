# Video Indexer (V2): Get Video Thumbnail

Retrieves a video thumbnail from Video Indexer (V2).

```
GET https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/get-video-thumbnail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Video Indexer (V2) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/get-video-thumbnail?connectionId=$CONNECTION_ID&location=string&accountId=string&videoId=string&thumbnailId=string&accessToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "location": "string",
  "accountId": "string",
  "videoId": "string",
  "thumbnailId": "string",
  "accessToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/get-video-thumbnail?${params}`, {
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
| `location` | string | yes | Indicates the Azure region to which the call should be routed. |
| `accountId` | string | yes | Video Indexer account ID. |
| `videoId` | string | yes | The video ID. |
| `thumbnailId` | string | yes | The thumbnail ID. |
| `accessToken` | string | yes | An account access token with read permissions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Video Indexer (V2) API, this operation is `GET /:location/Accounts/:accountId/Videos/:videoId/Thumbnails/:thumbnailId` (base URL `https://api.videoindexer.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-thumbnail.md) for the provider-specific parameters and requirements.

