# Miro: Get Board

Retrieves a board from Miro.

```
GET https://connect.mindcloud.co/v1/universal/miro/latest/actions/get-board
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Miro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/miro/latest/actions/get-board?connectionId=$CONNECTION_ID&boardId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "boardId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/miro/latest/actions/get-board?${params}`, {
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
| `boardId` | string | yes | Target board ID. |

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
      "lastOpenedAt": "2026-05-07T12:00:00.000Z",
      "lastOpenedBy": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
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
| `lastOpenedAt` | date |  |
| `lastOpenedBy.id` | string |  |
| `lastOpenedBy.name` | string |  |
| `lastOpenedBy.type` | string |  |
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

Through the native Miro API, this operation is `GET /boards/:board_id` (base URL `https://api.miro.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-board.md) for the provider-specific parameters and requirements.

