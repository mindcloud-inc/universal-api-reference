# Twist: List Threads

Retrieves threads from a Twist channel or workspace.

```
GET https://connect.mindcloud.co/v1/universal/twist/latest/actions/list-threads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twist/latest/actions/list-threads?connectionId=$CONNECTION_ID&channelId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twist/latest/actions/list-threads?${params}`, {
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
| `afterId` | number | no | Limits threads to those with a higher id than the specified id. |
| `asIds` | boolean | no | If enabled, only the ids of the threads are returned. |
| `beforeId` | number | no | Limits threads to those with a lower id than the specified id. |
| `channelId` | number | yes | The id of the channel. |
| `excludeThreadIds` | list<number> | no | Thread ids that should be excluded from the results. |
| `filterBy` | string | no | A filter can be one of attached_to_me or everyone. |
| `isPinned` | boolean | no | If enabled, only pinned threads are returned. |
| `isStarred` | boolean | no | If enabled, only starred threads are returned. |
| `limit` | number | no | Limits the number of threads returned. |
| `newerThanTs` | number | no | Limits threads to those newer than the specified Unix time. |
| `olderThanTs` | number | no | Limits threads to those older than the specified Unix time. |
| `orderBy` | string | no | Either desc or asc based on last_updated. |
| `workspaceId` | number | no | The id of the workspace. |

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

Through the native Twist API, this operation is `GET /threads/get` (base URL `https://api.twist.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-threads.md) for the provider-specific parameters and requirements.

