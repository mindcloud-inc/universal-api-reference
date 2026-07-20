# Video Indexer (V2): Get Video Index

Retrieves a video's index from Video Indexer (V2).

```
GET https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/get-video-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Video Indexer (V2) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/get-video-index?connectionId=$CONNECTION_ID&location=string&accountId=string&videoId=string&accessToken=string" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/get-video-index?${params}`, {
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
| `accessToken` | string | yes | An account access token with read permissions. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language` | string | no | The language of the captions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "created": "string",
      "description": {},
      "duration": "string",
      "durationInSeconds": 1,
      "id": "string",
      "isBase": true,
      "isEditable": true,
      "isOwned": true,
      "name": "Ava Chen",
      "partition": {},
      "privacyMode": "string",
      "state": "string",
      "summarizedInsights": {
        "duration": {
          "seconds": 1,
          "time": "string"
        },
        "id": "string",
        "labels": [
          {
            "appearances": [
              {
                "confidence": 1,
                "endSeconds": 1,
                "endTime": "string",
                "startSeconds": 1,
                "startTime": "string"
              }
            ],
            "id": 1,
            "name": "Ava Chen"
          }
        ],
        "name": "Ava Chen",
        "privacyMode": "string",
        "statistics": {
          "correspondenceCount": 1
        },
        "thumbnailId": "string",
        "thumbnailVideoId": "string"
      },
      "userName": "Ava Chen",
      "videos": [
        {
          "accountId": "string",
          "detectSourceLanguage": true,
          "externalId": "string",
          "externalUrl": {},
          "failureMessage": "string",
          "height": 1,
          "id": "string",
          "indexingPreset": "string",
          "insights": {
            "blocks": [
              {
                "id": 1,
                "instances": [
                  {
                    "adjustedEnd": "string",
                    "adjustedStart": "string",
                    "end": "string",
                    "start": "string"
                  }
                ]
              }
            ],
            "detectedObjects": [
              {
                "displayName": "Ava Chen",
                "id": 1,
                "instances": [
                  {
                    "adjustedEnd": "string",
                    "adjustedStart": "string",
                    "confidence": 1,
                    "end": "string",
                    "start": "string"
                  }
                ],
                "thumbnailId": "string",
                "type": "string",
                "wikiDataId": "string"
              }
            ],
            "duration": "string",
            "labels": [
              {
                "id": 1,
                "instances": [
                  {
                    "adjustedEnd": "string",
                    "adjustedStart": "string",
                    "confidence": 1,
                    "end": "string",
                    "start": "string"
                  }
                ],
                "language": "string",
                "name": "Ava Chen"
              }
            ],
            "language": "string",
            "languages": [
              "string"
            ],
            "scenes": [
              {
                "id": 1,
                "instances": [
                  {
                    "adjustedEnd": "string",
                    "adjustedStart": "string",
                    "end": "string",
                    "start": "string"
                  }
                ]
              }
            ],
            "shots": [
              {
                "id": 1,
                "instances": [
                  {
                    "adjustedEnd": "string",
                    "adjustedStart": "string",
                    "end": "string",
                    "start": "string"
                  }
                ],
                "keyFrames": [
                  {
                    "id": 1,
                    "instances": [
                      {
                        "adjustedEnd": "string",
                        "adjustedStart": "string",
                        "end": "string",
                        "start": "string",
                        "thumbnailId": "string"
                      }
                    ]
                  }
                ]
              }
            ],
            "sourceLanguage": "string",
            "sourceLanguages": [
              "string"
            ],
            "statistics": {
              "correspondenceCount": 1
            },
            "textualContentModeration": {
              "bannedWordsCount": 1,
              "bannedWordsRatio": 1,
              "id": 1
            },
            "version": "string"
          },
          "isAdult": true,
          "isSearchable": true,
          "language": "string",
          "languageAutoDetectMode": "string",
          "languages": [
            "string"
          ],
          "linguisticModelId": "string",
          "logoGroupId": {},
          "metadata": {},
          "moderationState": "string",
          "personModelId": "string",
          "privacyMode": "string",
          "processingProgress": "string",
          "publishedProxyUrl": {},
          "publishedUrl": "https://example.com",
          "reviewState": "string",
          "sourceLanguage": "string",
          "sourceLanguages": [
            "string"
          ],
          "state": "string",
          "streamingPreset": "string",
          "thumbnailId": "string",
          "viewToken": "string",
          "width": 1
        }
      ],
      "videosRanges": [
        {
          "range": {
            "end": "string",
            "start": "string"
          },
          "videoId": "string"
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
| `accountId` | string |  |
| `created` | string |  |
| `description` | object |  |
| `duration` | string |  |
| `durationInSeconds` | number |  |
| `id` | string |  |
| `isBase` | boolean |  |
| `isEditable` | boolean |  |
| `isOwned` | boolean |  |
| `name` | string |  |
| `partition` | object |  |
| `privacyMode` | string |  |
| `state` | string |  |
| `summarizedInsights.duration.seconds` | number |  |
| `summarizedInsights.duration.time` | string |  |
| `summarizedInsights.id` | string |  |
| `summarizedInsights.labels[].appearances[].confidence` | number |  |
| `summarizedInsights.labels[].appearances[].endSeconds` | number |  |
| `summarizedInsights.labels[].appearances[].endTime` | string |  |
| `summarizedInsights.labels[].appearances[].startSeconds` | number |  |
| `summarizedInsights.labels[].appearances[].startTime` | string |  |
| `summarizedInsights.labels[].id` | number |  |
| `summarizedInsights.labels[].name` | string |  |
| `summarizedInsights.name` | string |  |
| `summarizedInsights.privacyMode` | string |  |
| `summarizedInsights.statistics.correspondenceCount` | number |  |
| `summarizedInsights.thumbnailId` | string |  |
| `summarizedInsights.thumbnailVideoId` | string |  |
| `userName` | string |  |
| `videos[].accountId` | string |  |
| `videos[].detectSourceLanguage` | boolean |  |
| `videos[].externalId` | string |  |
| `videos[].externalUrl` | object |  |
| `videos[].failureMessage` | string |  |
| `videos[].height` | number |  |
| `videos[].id` | string |  |
| `videos[].indexingPreset` | string |  |
| `videos[].insights.blocks[].id` | number |  |
| `videos[].insights.blocks[].instances[].adjustedEnd` | string |  |
| `videos[].insights.blocks[].instances[].adjustedStart` | string |  |
| `videos[].insights.blocks[].instances[].end` | string |  |
| `videos[].insights.blocks[].instances[].start` | string |  |
| `videos[].insights.detectedObjects[].displayName` | string |  |
| `videos[].insights.detectedObjects[].id` | number |  |
| `videos[].insights.detectedObjects[].instances[].adjustedEnd` | string |  |
| `videos[].insights.detectedObjects[].instances[].adjustedStart` | string |  |
| `videos[].insights.detectedObjects[].instances[].confidence` | number |  |
| `videos[].insights.detectedObjects[].instances[].end` | string |  |
| `videos[].insights.detectedObjects[].instances[].start` | string |  |
| `videos[].insights.detectedObjects[].thumbnailId` | string |  |
| `videos[].insights.detectedObjects[].type` | string |  |
| `videos[].insights.detectedObjects[].wikiDataId` | string |  |
| `videos[].insights.duration` | string |  |
| `videos[].insights.labels[].id` | number |  |
| `videos[].insights.labels[].instances[].adjustedEnd` | string |  |
| `videos[].insights.labels[].instances[].adjustedStart` | string |  |
| `videos[].insights.labels[].instances[].confidence` | number |  |
| `videos[].insights.labels[].instances[].end` | string |  |
| `videos[].insights.labels[].instances[].start` | string |  |
| `videos[].insights.labels[].language` | string |  |
| `videos[].insights.labels[].name` | string |  |
| `videos[].insights.language` | string |  |
| `videos[].insights.languages[]` | string |  |
| `videos[].insights.scenes[].id` | number |  |
| `videos[].insights.scenes[].instances[].adjustedEnd` | string |  |
| `videos[].insights.scenes[].instances[].adjustedStart` | string |  |
| `videos[].insights.scenes[].instances[].end` | string |  |
| `videos[].insights.scenes[].instances[].start` | string |  |
| `videos[].insights.shots[].id` | number |  |
| `videos[].insights.shots[].instances[].adjustedEnd` | string |  |
| `videos[].insights.shots[].instances[].adjustedStart` | string |  |
| `videos[].insights.shots[].instances[].end` | string |  |
| `videos[].insights.shots[].instances[].start` | string |  |
| `videos[].insights.shots[].keyFrames[].id` | number |  |
| `videos[].insights.shots[].keyFrames[].instances[].adjustedEnd` | string |  |
| `videos[].insights.shots[].keyFrames[].instances[].adjustedStart` | string |  |
| `videos[].insights.shots[].keyFrames[].instances[].end` | string |  |
| `videos[].insights.shots[].keyFrames[].instances[].start` | string |  |
| `videos[].insights.shots[].keyFrames[].instances[].thumbnailId` | string |  |
| `videos[].insights.sourceLanguage` | string |  |
| `videos[].insights.sourceLanguages[]` | string |  |
| `videos[].insights.statistics.correspondenceCount` | number |  |
| `videos[].insights.textualContentModeration.bannedWordsCount` | number |  |
| `videos[].insights.textualContentModeration.bannedWordsRatio` | number |  |
| `videos[].insights.textualContentModeration.id` | number |  |
| `videos[].insights.version` | string |  |
| `videos[].isAdult` | boolean |  |
| `videos[].isSearchable` | boolean |  |
| `videos[].language` | string |  |
| `videos[].languageAutoDetectMode` | string |  |
| `videos[].languages[]` | string |  |
| `videos[].linguisticModelId` | string |  |
| `videos[].logoGroupId` | object |  |
| `videos[].metadata` | object |  |
| `videos[].moderationState` | string |  |
| `videos[].personModelId` | string |  |
| `videos[].privacyMode` | string |  |
| `videos[].processingProgress` | string |  |
| `videos[].publishedProxyUrl` | object |  |
| `videos[].publishedUrl` | string |  |
| `videos[].reviewState` | string |  |
| `videos[].sourceLanguage` | string |  |
| `videos[].sourceLanguages[]` | string |  |
| `videos[].state` | string |  |
| `videos[].streamingPreset` | string |  |
| `videos[].thumbnailId` | string |  |
| `videos[].viewToken` | string |  |
| `videos[].width` | number |  |
| `videosRanges[].range.end` | string |  |
| `videosRanges[].range.start` | string |  |
| `videosRanges[].videoId` | string |  |

## Native endpoint

Through the native Video Indexer (V2) API, this operation is `GET /:location/Accounts/:accountId/Videos/:videoId/Index` (base URL `https://api.videoindexer.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-index.md) for the provider-specific parameters and requirements.

