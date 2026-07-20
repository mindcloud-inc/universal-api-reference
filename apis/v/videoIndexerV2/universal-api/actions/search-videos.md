# Video Indexer (V2): Search Videos

Finds videos in Video Indexer (V2) by query.

```
GET https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/search-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Video Indexer (V2) `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/search-videos?connectionId=$CONNECTION_ID&limit=25&offset=0&location=string&accountId=string&accessToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "location": "string",
  "accountId": "string",
  "accessToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/search-videos?${params}`, {
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
| `accessToken` | string | yes | An account access token with read permissions. |
| `externalId` | string | no | An external ID associated with a video. |
| `query` | string | no | Free text to search for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `privacy` | string | no | The video privacy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPage": {
        "done": true,
        "pageSize": 1,
        "skip": 1,
        "totalCount": 1
      },
      "results": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPage.done` | boolean |  |
| `nextPage.pageSize` | number |  |
| `nextPage.skip` | number |  |
| `nextPage.totalCount` | number |  |
| `results[].accountId` | string |  |
| `results[].created` | string |  |
| `results[].description` | object |  |
| `results[].durationInSeconds` | number |  |
| `results[].externalId` | string |  |
| `results[].hasSourceVideoFile` | boolean |  |
| `results[].id` | string |  |
| `results[].indexingPreset` | string |  |
| `results[].isBase` | boolean |  |
| `results[].isOwned` | boolean |  |
| `results[].isSearchable` | boolean |  |
| `results[].lastIndexed` | string |  |
| `results[].lastModified` | string |  |
| `results[].metadata` | object |  |
| `results[].moderationState` | string |  |
| `results[].name` | string |  |
| `results[].partition` | object |  |
| `results[].personModelId` | string |  |
| `results[].privacyMode` | string |  |
| `results[].processingProgress` | string |  |
| `results[].reviewState` | string |  |
| `results[].sourceLanguage` | string |  |
| `results[].sourceLanguages[]` | string |  |
| `results[].state` | string |  |
| `results[].streamingPreset` | string |  |
| `results[].thumbnailId` | string |  |
| `results[].thumbnailVideoId` | string |  |
| `results[].userName` | string |  |

## Native endpoint

Through the native Video Indexer (V2) API, this operation is `GET /:location/Accounts/:accountId/Videos/Search` (base URL `https://api.videoindexer.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-videos.md) for the provider-specific parameters and requirements.

