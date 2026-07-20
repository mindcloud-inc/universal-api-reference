# Speak Ai: List Media

Retrieves media from Speak Ai.

```
GET https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/list-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speak Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/list-media?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/list-media?${params}`, {
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
| `mediaType` | string | no | Filter media by type such as audio or video. |
| `folderId` | string | no | Restrict the list to media inside a specific folder. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filterMedia` | string | no | Filter the list using Speak Ai's media filter value. |
| `filterName` | string | no | Filter media by name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mediaList": [
        {
          "count": {
            "characterCount": 1,
            "characterCountWithoutSpace": 1,
            "wordCount": 1
          },
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "duration": {
            "inSecond": 1
          },
          "folderId": "string",
          "isFavorite": true,
          "mediaId": "string",
          "mediaType": "string",
          "name": "Ava Chen",
          "originalCreatedAt": "2026-05-07T12:00:00.000Z",
          "privacyMode": "string",
          "processingProgress": "string",
          "remark": "string",
          "size": 1,
          "sourceLanguage": "string",
          "state": "string",
          "tags": [
            "string"
          ],
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "pages": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mediaList[].count.characterCount` | number |  |
| `mediaList[].count.characterCountWithoutSpace` | number |  |
| `mediaList[].count.wordCount` | number |  |
| `mediaList[].createdAt` | date |  |
| `mediaList[].description` | string |  |
| `mediaList[].duration.inSecond` | number |  |
| `mediaList[].folderId` | string |  |
| `mediaList[].isFavorite` | boolean |  |
| `mediaList[].mediaId` | string |  |
| `mediaList[].mediaType` | string |  |
| `mediaList[].name` | string |  |
| `mediaList[].originalCreatedAt` | date |  |
| `mediaList[].privacyMode` | string |  |
| `mediaList[].processingProgress` | string |  |
| `mediaList[].remark` | string |  |
| `mediaList[].size` | number |  |
| `mediaList[].sourceLanguage` | string |  |
| `mediaList[].state` | string |  |
| `mediaList[].tags[]` | string |  |
| `mediaList[].updatedAt` | date |  |
| `pages` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Speak Ai API, this operation is `GET /media` (base URL `https://api.speakai.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-media.md) for the provider-specific parameters and requirements.

