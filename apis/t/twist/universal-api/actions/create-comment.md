# Twist: Create Comment

Creates a new comment in a Twist thread.

```
POST https://connect.mindcloud.co/v1/universal/twist/latest/actions/create-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/twist/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "threadId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twist/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "threadId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachments` | string | no | JSON-encoded list of attachment objects returned by Upload attachment. |
| `content` | string | yes | The content of the new comment. |
| `recipients` | string | no | Users to notify. |
| `sendAsIntegration` | boolean | no | Displays the integration as the comment creator. |
| `threadAction` | string | no | Can be close or reopen. |
| `threadId` | number | yes | The id of the thread. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelId": 1,
      "content": "string",
      "creator": 1,
      "creatorName": "Ava Chen",
      "deleted": true,
      "id": 1,
      "objIndex": 1,
      "postedTs": "string",
      "systemMessage": {
        "channelId": 1,
        "channelName": "Ava Chen",
        "initiator": "string",
        "initiatorId": 1,
        "initiatorName": "Ava Chen",
        "newTitle": "string",
        "oldTitle": "string",
        "type": "string"
      },
      "threadId": 1,
      "version": 1,
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelId` | number |  |
| `content` | string |  |
| `creator` | number |  |
| `creatorName` | string |  |
| `deleted` | boolean |  |
| `id` | number |  |
| `objIndex` | number |  |
| `postedTs` | string |  |
| `systemMessage.channelId` | number |  |
| `systemMessage.channelName` | string |  |
| `systemMessage.initiator` | string |  |
| `systemMessage.initiatorId` | number |  |
| `systemMessage.initiatorName` | string |  |
| `systemMessage.newTitle` | string |  |
| `systemMessage.oldTitle` | string |  |
| `systemMessage.type` | string |  |
| `threadId` | number |  |
| `version` | number |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native Twist API, this operation is `POST /comments/add` (base URL `https://api.twist.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comment.md) for the provider-specific parameters and requirements.

