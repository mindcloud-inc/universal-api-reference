# Zenkit: Create List Entry Comment

Creates a comment on a Zenkit item.

```
POST https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/create-list-entry-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/create-list-entry-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listAllId": "string",
  "listEntryAllId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/create-list-entry-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listAllId": "string",
    "listEntryAllId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listAllId` | string | yes | The list all id |
| `listEntryAllId` | string | yes | The list entry all id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bulk_rowcount": "string",
      "changedData": "string",
      "changedDataElementId": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_in": 1,
      "deprecated_at": "string",
      "id": 1,
      "isBulk": true,
      "listDeprecated_at": "string",
      "listDescription": "string",
      "listEntryDeprecated_at": "string",
      "listEntryDisplayString": "string",
      "listEntryId": 1,
      "listEntryShortId": "string",
      "listEntryUUID": "string",
      "listId": 1,
      "listName": "Ava Chen",
      "listShortId": "string",
      "listType": "string",
      "listUUID": "string",
      "message": "string",
      "messageTextType": "string",
      "originData": "string",
      "originProvider": "string",
      "parentUUID": "string",
      "shortId": "string",
      "type": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "userDisplayname": "Ava Chen",
      "userFullname": "Ava Chen",
      "userId": 1,
      "userImagelink": "https://example.com",
      "userInitials": "string",
      "userIsImagePreferred": true,
      "userUsername": "Ava Chen",
      "uuid": "string",
      "workspaceDeprecated_at": "string",
      "workspaceDescription": "string",
      "workspaceId": 1,
      "workspaceName": "Ava Chen",
      "workspaceShortId": "string",
      "workspaceType": "string",
      "workspaceUUID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bulk_rowcount` | string |  |
| `changedData` | string |  |
| `changedDataElementId` | string |  |
| `created_at` | date |  |
| `created_in` | number |  |
| `deprecated_at` | string |  |
| `id` | number |  |
| `isBulk` | boolean |  |
| `listDeprecated_at` | string |  |
| `listDescription` | string |  |
| `listEntryDeprecated_at` | string |  |
| `listEntryDisplayString` | string |  |
| `listEntryId` | number |  |
| `listEntryShortId` | string |  |
| `listEntryUUID` | string |  |
| `listId` | number |  |
| `listName` | string |  |
| `listShortId` | string |  |
| `listType` | string |  |
| `listUUID` | string |  |
| `message` | string |  |
| `messageTextType` | string |  |
| `originData` | string |  |
| `originProvider` | string |  |
| `parentUUID` | string |  |
| `shortId` | string |  |
| `type` | number |  |
| `updated_at` | date |  |
| `userDisplayname` | string |  |
| `userFullname` | string |  |
| `userId` | number |  |
| `userImagelink` | string |  |
| `userInitials` | string |  |
| `userIsImagePreferred` | boolean |  |
| `userUsername` | string |  |
| `uuid` | string |  |
| `workspaceDeprecated_at` | string |  |
| `workspaceDescription` | string |  |
| `workspaceId` | number |  |
| `workspaceName` | string |  |
| `workspaceShortId` | string |  |
| `workspaceType` | string |  |
| `workspaceUUID` | string |  |

## Native endpoint

Through the native Zenkit API, this operation is `POST /users/me/lists/:listAllId/entries/:listEntryAllId/activities` (base URL `https://zenkit.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list-entry-comment.md) for the provider-specific parameters and requirements.

