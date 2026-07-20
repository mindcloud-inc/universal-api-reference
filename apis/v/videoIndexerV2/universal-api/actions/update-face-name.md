# Video Indexer (V2): Update Face Name

Updates a face name in Video Indexer (V2).

```
PUT https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/update-face-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Video Indexer (V2) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/update-face-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "location": "string",
  "accountId": "string",
  "videoId": "string",
  "faceId": 1,
  "accessToken": "string",
  "newName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/update-face-name', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "location": "string",
    "accountId": "string",
    "videoId": "string",
    "faceId": 1,
    "accessToken": "string",
    "newName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `location` | string | yes | Indicates the Azure region to which the call should be routed. |
| `accountId` | string | yes | Video Indexer account ID. |
| `videoId` | string | yes | The video ID. |
| `faceId` | number | yes | The face ID. |
| `accessToken` | string | yes | An account access token with write permissions. |
| `newName` | string | yes | A new name for the face. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Video Indexer (V2) API returns.

## Native endpoint

Through the native Video Indexer (V2) API, this operation is `PUT /:location/Accounts/:accountId/Videos/:videoId/Index/Faces/:faceId` (base URL `https://api.videoindexer.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-face-name.md) for the provider-specific parameters and requirements.

