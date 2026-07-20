# Twist: Move Thread to Channel

Moves a thread to another Twist channel.

```
PUT https://connect.mindcloud.co/v1/universal/twist/latest/actions/move-thread-to-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/twist/latest/actions/move-thread-to-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "threadId": 1,
  "toChannelId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twist/latest/actions/move-thread-to-channel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "threadId": 1,
    "toChannelId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threadId` | number | yes | The id of the thread. |
| `toChannelId` | number | yes | The target channel's id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelId": 1,
      "closed": true,
      "commentCount": 1,
      "content": "string",
      "creator": 1,
      "creatorName": "Ava Chen",
      "groups": [
        1
      ],
      "id": 1,
      "inInbox": true,
      "isArchived": true,
      "isSaved": true,
      "lastComment": {
        "channelId": 1,
        "content": "string",
        "creator": 1,
        "creatorName": "Ava Chen",
        "deleted": true,
        "id": 1,
        "objIndex": 1,
        "postedTs": 1,
        "systemMessage": {
          "channelId": 1,
          "channelName": "Ava Chen",
          "initiator": 1,
          "initiatorId": 1,
          "initiatorName": "Ava Chen",
          "type": "string"
        },
        "threadId": 1,
        "version": 1,
        "workspaceId": 1
      },
      "lastEditedTs": 1,
      "lastObjIndex": 1,
      "lastUpdatedTs": 1,
      "participants": [
        1
      ],
      "pinned": true,
      "postedTs": 1,
      "responders": [
        1
      ],
      "snippet": "string",
      "snippetCreator": 1,
      "starred": true,
      "title": "string",
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
| `closed` | boolean |  |
| `commentCount` | number |  |
| `content` | string |  |
| `creator` | number |  |
| `creatorName` | string |  |
| `groups[]` | number |  |
| `id` | number |  |
| `inInbox` | boolean |  |
| `isArchived` | boolean |  |
| `isSaved` | boolean |  |
| `lastComment.channelId` | number |  |
| `lastComment.content` | string |  |
| `lastComment.creator` | number |  |
| `lastComment.creatorName` | string |  |
| `lastComment.deleted` | boolean |  |
| `lastComment.id` | number |  |
| `lastComment.objIndex` | number |  |
| `lastComment.postedTs` | number |  |
| `lastComment.systemMessage.channelId` | number |  |
| `lastComment.systemMessage.channelName` | string |  |
| `lastComment.systemMessage.initiator` | number |  |
| `lastComment.systemMessage.initiatorId` | number |  |
| `lastComment.systemMessage.initiatorName` | string |  |
| `lastComment.systemMessage.type` | string |  |
| `lastComment.threadId` | number |  |
| `lastComment.version` | number |  |
| `lastComment.workspaceId` | number |  |
| `lastEditedTs` | number |  |
| `lastObjIndex` | number |  |
| `lastUpdatedTs` | number |  |
| `participants[]` | number |  |
| `pinned` | boolean |  |
| `postedTs` | number |  |
| `responders[]` | number |  |
| `snippet` | string |  |
| `snippetCreator` | number |  |
| `starred` | boolean |  |
| `title` | string |  |
| `version` | number |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native Twist API, this operation is `POST /threads/move_to_channel` (base URL `https://api.twist.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-thread-to-channel.md) for the provider-specific parameters and requirements.

