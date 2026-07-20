# Speak Ai: Get Text Insight

Retrieves text insights from Speak Ai.

```
GET https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/get-text-insight
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speak Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/get-text-insight?connectionId=$CONNECTION_ID&mediaId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/get-text-insight?${params}`, {
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
| `mediaId` | string | yes | Speak Ai text note media identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": {
        "characterCount": 1,
        "characterCountWithoutSpace": 1,
        "wordCount": 1
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "folderId": "string",
      "insight": {
        "keywords": [
          {
            "id": 1,
            "instances": [
              {
                "endChar": 1,
                "startChar": 1
              }
            ],
            "isCustom": true,
            "isDeleted": true,
            "name": "Ava Chen"
          }
        ]
      },
      "mediaId": "string",
      "name": "Ava Chen",
      "originalCreatedAt": "2026-05-07T12:00:00.000Z",
      "rawText": "string",
      "remark": "string",
      "sourceLanguage": "string",
      "state": "string",
      "text": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count.characterCount` | number |  |
| `count.characterCountWithoutSpace` | number |  |
| `count.wordCount` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `folderId` | string |  |
| `insight.keywords[].id` | number |  |
| `insight.keywords[].instances[].endChar` | number |  |
| `insight.keywords[].instances[].startChar` | number |  |
| `insight.keywords[].isCustom` | boolean |  |
| `insight.keywords[].isDeleted` | boolean |  |
| `insight.keywords[].name` | string |  |
| `mediaId` | string |  |
| `name` | string |  |
| `originalCreatedAt` | date |  |
| `rawText` | string |  |
| `remark` | string |  |
| `sourceLanguage` | string |  |
| `state` | string |  |
| `text` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Speak Ai API, this operation is `GET /text/insight/:mediaId` (base URL `https://api.speakai.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-text-insight.md) for the provider-specific parameters and requirements.

