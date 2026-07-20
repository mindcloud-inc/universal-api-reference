# Twist: Get or Create Conversation

Finds a Twist conversation, or creates one if needed.

```
POST https://connect.mindcloud.co/v1/universal/twist/latest/actions/get-or-create-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/twist/latest/actions/get-or-create-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userIds": "string",
  "workspaceId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twist/latest/actions/get-or-create-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userIds": "string",
    "workspaceId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userIds` | string<number> | yes | JSON-encoded list of user IDs, for example [10073,10076]. |
| `workspaceId` | number | yes | The id of the workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdTs": "string",
      "creator": 1,
      "id": 1,
      "lastActiveTs": "string",
      "lastMessage": {
        "attachments": [
          {
            "attachmentId": "string",
            "fileName": "Ava Chen",
            "fileSize": 1,
            "title": "string",
            "underlyingType": "string",
            "uploadState": "string",
            "url": "https://example.com",
            "urlType": "https://example.com"
          }
        ],
        "content": "string",
        "conversationId": 1,
        "creator": 1,
        "creatorName": "Ava Chen",
        "deleted": true,
        "id": 1,
        "objIndex": 1,
        "postedTs": "string",
        "version": 1,
        "workspaceId": 1
      },
      "lastObjIndex": 1,
      "private": true,
      "snippet": "string",
      "snippetCreators": [
        1
      ],
      "title": "string",
      "userIds": [
        1
      ],
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
| `archived` | boolean |  |
| `createdTs` | string |  |
| `creator` | number |  |
| `id` | number |  |
| `lastActiveTs` | string |  |
| `lastMessage.attachments[].attachmentId` | string |  |
| `lastMessage.attachments[].fileName` | string |  |
| `lastMessage.attachments[].fileSize` | number |  |
| `lastMessage.attachments[].title` | string |  |
| `lastMessage.attachments[].underlyingType` | string |  |
| `lastMessage.attachments[].uploadState` | string |  |
| `lastMessage.attachments[].url` | string |  |
| `lastMessage.attachments[].urlType` | string |  |
| `lastMessage.content` | string |  |
| `lastMessage.conversationId` | number |  |
| `lastMessage.creator` | number |  |
| `lastMessage.creatorName` | string |  |
| `lastMessage.deleted` | boolean |  |
| `lastMessage.id` | number |  |
| `lastMessage.objIndex` | number |  |
| `lastMessage.postedTs` | string |  |
| `lastMessage.version` | number |  |
| `lastMessage.workspaceId` | number |  |
| `lastObjIndex` | number |  |
| `private` | boolean |  |
| `snippet` | string |  |
| `snippetCreators[]` | number |  |
| `title` | string |  |
| `userIds[]` | number |  |
| `version` | number |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native Twist API, this operation is `POST /conversations/get_or_create` (base URL `https://api.twist.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-or-create-conversation.md) for the provider-specific parameters and requirements.

