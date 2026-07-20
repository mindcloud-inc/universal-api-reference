# Miro: Create Board

Creates a new board in Miro.

```
POST https://connect.mindcloud.co/v1/universal/miro/latest/actions/create-board
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Miro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/miro/latest/actions/create-board" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/miro/latest/actions/create-board', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Board name |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional board description |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "currentUserMembership": {
        "id": "string",
        "name": "Ava Chen",
        "role": "string",
        "type": "string"
      },
      "description": "string",
      "id": "string",
      "links": {
        "related": "https://example.com",
        "self": "https://example.com"
      },
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "modifiedBy": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "name": "Ava Chen",
      "owner": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "permissionsPolicy": {
        "collaborationToolsStartAccess": "string",
        "copyAccess": "string",
        "copyAccessLevel": "string",
        "sharingAccess": "string"
      },
      "picture": {
        "id": 1,
        "imageURL": "https://example.com"
      },
      "policy": {
        "permissionsPolicy": {
          "collaborationToolsStartAccess": "string",
          "copyAccess": "string",
          "copyAccessLevel": "string",
          "sharingAccess": "string"
        },
        "sharingPolicy": {
          "access": "string",
          "accessPasswordRequired": true,
          "inviteToAccountAndBoardLinkAccess": "https://example.com",
          "organizationAccess": "string",
          "teamAccess": "string"
        }
      },
      "project": {
        "id": "string"
      },
      "sharingPolicy": {
        "access": "string",
        "accessPasswordRequired": true,
        "inviteToAccountAndBoardLinkAccess": "https://example.com",
        "organizationAccess": "string",
        "teamAccess": "string"
      },
      "team": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "type": "string",
      "viewLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy.id` | string |  |
| `createdBy.name` | string |  |
| `createdBy.type` | string |  |
| `currentUserMembership.id` | string |  |
| `currentUserMembership.name` | string |  |
| `currentUserMembership.role` | string |  |
| `currentUserMembership.type` | string |  |
| `description` | string |  |
| `id` | string |  |
| `links.related` | string |  |
| `links.self` | string |  |
| `modifiedAt` | date |  |
| `modifiedBy.id` | string |  |
| `modifiedBy.name` | string |  |
| `modifiedBy.type` | string |  |
| `name` | string |  |
| `owner.id` | string |  |
| `owner.name` | string |  |
| `owner.type` | string |  |
| `permissionsPolicy.collaborationToolsStartAccess` | string |  |
| `permissionsPolicy.copyAccess` | string |  |
| `permissionsPolicy.copyAccessLevel` | string |  |
| `permissionsPolicy.sharingAccess` | string |  |
| `picture.id` | number |  |
| `picture.imageURL` | string |  |
| `policy.permissionsPolicy.collaborationToolsStartAccess` | string |  |
| `policy.permissionsPolicy.copyAccess` | string |  |
| `policy.permissionsPolicy.copyAccessLevel` | string |  |
| `policy.permissionsPolicy.sharingAccess` | string |  |
| `policy.sharingPolicy.access` | string |  |
| `policy.sharingPolicy.accessPasswordRequired` | boolean |  |
| `policy.sharingPolicy.inviteToAccountAndBoardLinkAccess` | string |  |
| `policy.sharingPolicy.organizationAccess` | string |  |
| `policy.sharingPolicy.teamAccess` | string |  |
| `project.id` | string |  |
| `sharingPolicy.access` | string |  |
| `sharingPolicy.accessPasswordRequired` | boolean |  |
| `sharingPolicy.inviteToAccountAndBoardLinkAccess` | string |  |
| `sharingPolicy.organizationAccess` | string |  |
| `sharingPolicy.teamAccess` | string |  |
| `team.id` | string |  |
| `team.name` | string |  |
| `team.type` | string |  |
| `type` | string |  |
| `viewLink` | string |  |

## Native endpoint

Through the native Miro API, this operation is `POST /boards` (base URL `https://api.miro.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-board.md) for the provider-specific parameters and requirements.

