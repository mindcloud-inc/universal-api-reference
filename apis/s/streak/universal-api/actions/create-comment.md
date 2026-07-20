# Streak: Create Comment

Creates a new comment in Streak.

```
POST https://connect.mindcloud.co/v1/universal/streak/latest/actions/create-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/streak/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "boxKey": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/streak/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "boxKey": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `boxKey` | string | yes |  |
| `message` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `boxKey` | string | The box that owns the comment. |
| `commentKey` | string | The comment key. |
| `creatorKey` | string | The user who created the comment. |
| `key` | string | The comment key alias. |
| `lastSavedTimestamp` | date | When the comment was last saved. |
| `message` | string | The comment message. |
| `newsfeedEntryKey` | string | The related newsfeed entry key. |
| `pipelineKey` | string | The pipeline that owns the comment. |
| `reactionSummary` | array<object> | Reaction summary entries. |
| `timestamp` | date | When the comment was created. |

## Native endpoint

Through the native Streak API, this operation is `POST /api/v2/boxes/:boxKey/comments` (base URL `https://api.streak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comment.md) for the provider-specific parameters and requirements.

