# zipBoard: Create Response

Creates a new response in zipBoard.

```
POST https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reply": "string",
  "route": "string",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reply": "string",
    "route": "string",
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachments[]` | array<string> | no |  |
| `mentionedIds` | string<string> | no |  |
| `reply` | string | yes |  |
| `replyId` | string | no |  |
| `route` | string | yes |  |
| `taskId` | string | yes |  |
| `userId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "reply": "string",
      "taskid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Response identifier. |
| `reply` | string | Response body. |
| `taskid` | string | Task identifier. |

## Native endpoint

Through the native zipBoard API, this operation is `POST /issues/responses` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-response.md) for the provider-specific parameters and requirements.

