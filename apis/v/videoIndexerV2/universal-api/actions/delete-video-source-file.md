# Video Indexer (V2): Delete Video Source File

Deletes a video's source file from Video Indexer (V2).

```
DELETE https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/delete-video-source-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Video Indexer (V2) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/delete-video-source-file?connectionId=$CONNECTION_ID&location=string&accountId=string&videoId=string&accessToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "location": "string",
  "accountId": "string",
  "videoId": "string",
  "accessToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/delete-video-source-file?${params}`, {
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
| `accessToken` | string | yes | An account access token with write permissions. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Video Indexer (V2) API returns.

## Native endpoint

Through the native Video Indexer (V2) API, this operation is `DELETE /:location/Accounts/:accountId/Videos/:videoId/SourceFile` (base URL `https://api.videoindexer.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-video-source-file.md) for the provider-specific parameters and requirements.

