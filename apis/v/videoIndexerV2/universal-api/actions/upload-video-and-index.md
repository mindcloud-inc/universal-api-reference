# Video Indexer (V2): Upload Video And Index

Uploads and indexes a video in Video Indexer (V2).

```
POST https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/upload-video-and-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Video Indexer (V2) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/upload-video-and-index" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "location": "string",
  "accountId": "string",
  "accessToken": "string",
  "name": "Ava Chen",
  "videoUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/upload-video-and-index', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "location": "string",
    "accountId": "string",
    "accessToken": "string",
    "name": "Ava Chen",
    "videoUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `location` | string | yes | Azure region to route the call to. |
| `accountId` | string | yes | Video Indexer account ID. |
| `accessToken` | string | yes | Account access token with write permissions. |
| `name` | string | yes | The title of the video. |
| `videoUrl` | string | yes | A public URL of the video or audio file to index. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | no | An external ID associated with the uploaded video. |
| `privacy` | string | no | The video privacy. Default: `private`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "created": "string",
      "description": {},
      "durationInSeconds": 1,
      "externalId": "string",
      "hasSourceVideoFile": true,
      "id": "string",
      "indexingPreset": "string",
      "isBase": true,
      "isOwned": true,
      "isSearchable": true,
      "lastIndexed": "string",
      "lastModified": "string",
      "metadata": {},
      "moderationState": "string",
      "name": "Ava Chen",
      "partition": {},
      "personModelId": "string",
      "privacyMode": "string",
      "processingProgress": "string",
      "reviewState": "string",
      "sourceLanguage": "string",
      "sourceLanguages": [
        "string"
      ],
      "state": "string",
      "streamingPreset": "string",
      "thumbnailId": "string",
      "thumbnailVideoId": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `created` | string |  |
| `description` | object |  |
| `durationInSeconds` | number |  |
| `externalId` | string |  |
| `hasSourceVideoFile` | boolean |  |
| `id` | string |  |
| `indexingPreset` | string |  |
| `isBase` | boolean |  |
| `isOwned` | boolean |  |
| `isSearchable` | boolean |  |
| `lastIndexed` | string |  |
| `lastModified` | string |  |
| `metadata` | object |  |
| `moderationState` | string |  |
| `name` | string |  |
| `partition` | object |  |
| `personModelId` | string |  |
| `privacyMode` | string |  |
| `processingProgress` | string |  |
| `reviewState` | string |  |
| `sourceLanguage` | string |  |
| `sourceLanguages[]` | string |  |
| `state` | string |  |
| `streamingPreset` | string |  |
| `thumbnailId` | string |  |
| `thumbnailVideoId` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Video Indexer (V2) API, this operation is `POST /:location/Accounts/:accountId/Videos` (base URL `https://api.videoindexer.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-video-and-index.md) for the provider-specific parameters and requirements.

