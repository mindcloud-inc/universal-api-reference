# Twist: List Unread Threads

Retrieves unread threads from a Twist workspace.

```
GET https://connect.mindcloud.co/v1/universal/twist/latest/actions/list-unread-threads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twist/latest/actions/list-unread-threads?connectionId=$CONNECTION_ID&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twist/latest/actions/list-unread-threads?${params}`, {
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
| `workspaceId` | number | yes | The id of the workspace. |

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

Through the native Twist API, this operation is `GET /threads/get_unread` (base URL `https://api.twist.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unread-threads.md) for the provider-specific parameters and requirements.

