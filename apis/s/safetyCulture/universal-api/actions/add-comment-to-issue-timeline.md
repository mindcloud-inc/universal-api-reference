# SafetyCulture: Add Comment to Issue Timeline

Creates an issue timeline comment in SafetyCulture.

```
POST https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/add-comment-to-issue-timeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/add-comment-to-issue-timeline" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "comment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/add-comment-to-issue-timeline', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "comment": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | Required. The UUID for the task the comment is being added to. |
| `comment` | string | yes | Required. The content of the comment. |
| `createdAt` | date | no | Optional. Date/time this comment was added. |
| `eventId` | string | no | Optional. The unique identifier for the event. This will be auto-generated if omitted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object |  |

## Native endpoint

Through the native SafetyCulture API, this operation is `POST /tasks/v1/timeline/comments` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-comment-to-issue-timeline.md) for the provider-specific parameters and requirements.

