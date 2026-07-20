# Twist: List Comments

Retrieves comments from a Twist thread.

```
GET https://connect.mindcloud.co/v1/universal/twist/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twist/latest/actions/list-comments?connectionId=$CONNECTION_ID&threadId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "threadId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twist/latest/actions/list-comments?${params}`, {
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
| `limit` | number | no | Limits the number of comments returned. |
| `orderBy` | string | no | Either desc or asc based on obj_index. |
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

Through the native Twist API, this operation is `GET /comments/get` (base URL `https://api.twist.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

