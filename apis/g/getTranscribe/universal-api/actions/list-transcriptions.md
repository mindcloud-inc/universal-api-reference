# GetTranscribe: List Transcriptions

Retrieves transcriptions from GetTranscribe by filters.

```
GET https://connect.mindcloud.co/v1/universal/getTranscribe/latest/actions/list-transcriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetTranscribe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getTranscribe/latest/actions/list-transcriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getTranscribe/latest/actions/list-transcriptions?${params}`, {
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
| `folderId` | number | no | Filter transcriptions by folder ID. |
| `platform` | string | no | Filter transcriptions by source platform. One of: `0`, `1`, `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "authorId": "string",
      "channel": "string",
      "charCount": 1,
      "commentCount": 1,
      "consumptionType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "downloadMethod": "string",
      "duration": 1,
      "durationSeconds": 1,
      "folderId": 1,
      "generatedTitle": "string",
      "id": 1,
      "language": "string",
      "likeCount": 1,
      "platform": "string",
      "prompt": "string",
      "proxyProvider": "string",
      "proxyUsed": true,
      "relationFolder": {},
      "source": "string",
      "thumbnailUrl": "https://example.com",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uploadDate": "string",
      "uploadTimestamp": "string",
      "url": "https://example.com",
      "videoDescription": "string",
      "videoHeight": 1,
      "videoTitle": "string",
      "videoWidth": 1,
      "viewCount": 1,
      "wordCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `authorId` | string |  |
| `channel` | string |  |
| `charCount` | number |  |
| `commentCount` | number |  |
| `consumptionType` | string |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `downloadMethod` | string |  |
| `duration` | number |  |
| `durationSeconds` | number |  |
| `folderId` | number |  |
| `generatedTitle` | string |  |
| `id` | number |  |
| `language` | string |  |
| `likeCount` | number |  |
| `platform` | string |  |
| `prompt` | string |  |
| `proxyProvider` | string |  |
| `proxyUsed` | boolean |  |
| `relationFolder` | object |  |
| `source` | string |  |
| `thumbnailUrl` | string |  |
| `updatedAt` | date |  |
| `uploadDate` | string |  |
| `uploadTimestamp` | string |  |
| `url` | string |  |
| `videoDescription` | string |  |
| `videoHeight` | number |  |
| `videoTitle` | string |  |
| `videoWidth` | number |  |
| `viewCount` | number |  |
| `wordCount` | number |  |

## Native endpoint

Through the native GetTranscribe API, this operation is `GET /transcriptions` (base URL `https://api.gettranscribe.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transcriptions.md) for the provider-specific parameters and requirements.

