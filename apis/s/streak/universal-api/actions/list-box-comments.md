# Streak: List Box Comments

Retrieves comments for a box in Streak.

```
GET https://connect.mindcloud.co/v1/universal/streak/latest/actions/list-box-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streak/latest/actions/list-box-comments?connectionId=$CONNECTION_ID&boxKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "boxKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streak/latest/actions/list-box-comments?${params}`, {
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
| `boxKey` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasNextPage": true,
      "results": [
        {
          "boxKey": "string",
          "commentKey": "string",
          "creatorKey": "string",
          "key": "string",
          "lastSavedTimestamp": "2026-05-07T12:00:00.000Z",
          "message": "string",
          "newsfeedEntryKey": "string",
          "pipelineKey": "string",
          "reactionSummary": [
            {}
          ],
          "timestamp": "2026-05-07T12:00:00.000Z"
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
| `hasNextPage` | boolean | Whether more comments are available. |
| `results` | array<object> | Comments attached to the box. |
| `results[].boxKey` | string | The box that owns the comment. |
| `results[].commentKey` | string | The comment key. |
| `results[].creatorKey` | string | The user who created the comment. |
| `results[].key` | string | The comment key alias. |
| `results[].lastSavedTimestamp` | date | When the comment was last saved. |
| `results[].message` | string | The comment message. |
| `results[].newsfeedEntryKey` | string | The related newsfeed entry key. |
| `results[].pipelineKey` | string | The pipeline that owns the comment. |
| `results[].reactionSummary` | array<object> | Reaction summary entries. |
| `results[].timestamp` | date | When the comment was created. |

## Native endpoint

Through the native Streak API, this operation is `GET /api/v2/boxes/:boxKey/comments` (base URL `https://api.streak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-box-comments.md) for the provider-specific parameters and requirements.

