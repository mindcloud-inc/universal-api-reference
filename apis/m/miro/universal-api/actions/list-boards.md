# Miro: List Boards

Retrieves boards from Miro.

```
GET https://connect.mindcloud.co/v1/universal/miro/latest/actions/list-boards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Miro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/miro/latest/actions/list-boards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/miro/latest/actions/list-boards?${params}`, {
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
| `limit` | number | no | Maximum number of boards to return. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | Pagination cursor returned by the previous request. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "limit": 1,
      "links": {
        "first": "https://example.com",
        "last": "https://example.com",
        "next": "https://example.com",
        "prev": "https://example.com",
        "self": "https://example.com"
      },
      "offset": 1,
      "size": 1,
      "total": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].createdAt` | date |  |
| `data[].createdBy.id` | string |  |
| `data[].createdBy.name` | string |  |
| `data[].createdBy.type` | string |  |
| `data[].currentUserMembership.id` | string |  |
| `data[].currentUserMembership.name` | string |  |
| `data[].currentUserMembership.role` | string |  |
| `data[].currentUserMembership.type` | string |  |
| `data[].description` | string |  |
| `data[].id` | string |  |
| `data[].lastOpenedAt` | date |  |
| `data[].lastOpenedBy.id` | string |  |
| `data[].lastOpenedBy.name` | string |  |
| `data[].lastOpenedBy.type` | string |  |
| `data[].links.related` | string |  |
| `data[].links.self` | string |  |
| `data[].modifiedAt` | date |  |
| `data[].modifiedBy.id` | string |  |
| `data[].modifiedBy.name` | string |  |
| `data[].modifiedBy.type` | string |  |
| `data[].name` | string |  |
| `data[].owner.id` | string |  |
| `data[].owner.name` | string |  |
| `data[].owner.type` | string |  |
| `data[].permissionsPolicy.collaborationToolsStartAccess` | string |  |
| `data[].permissionsPolicy.copyAccess` | string |  |
| `data[].permissionsPolicy.copyAccessLevel` | string |  |
| `data[].permissionsPolicy.sharingAccess` | string |  |
| `data[].picture.id` | number |  |
| `data[].picture.imageURL` | string |  |
| `data[].policy.permissionsPolicy.collaborationToolsStartAccess` | string |  |
| `data[].policy.permissionsPolicy.copyAccess` | string |  |
| `data[].policy.permissionsPolicy.copyAccessLevel` | string |  |
| `data[].policy.permissionsPolicy.sharingAccess` | string |  |
| `data[].policy.sharingPolicy.access` | string |  |
| `data[].policy.sharingPolicy.accessPasswordRequired` | boolean |  |
| `data[].policy.sharingPolicy.inviteToAccountAndBoardLinkAccess` | string |  |
| `data[].policy.sharingPolicy.organizationAccess` | string |  |
| `data[].policy.sharingPolicy.teamAccess` | string |  |
| `data[].project.id` | string |  |
| `data[].sharingPolicy.access` | string |  |
| `data[].sharingPolicy.accessPasswordRequired` | boolean |  |
| `data[].sharingPolicy.inviteToAccountAndBoardLinkAccess` | string |  |
| `data[].sharingPolicy.organizationAccess` | string |  |
| `data[].sharingPolicy.teamAccess` | string |  |
| `data[].team.id` | string |  |
| `data[].team.name` | string |  |
| `data[].team.type` | string |  |
| `data[].type` | string |  |
| `data[].viewLink` | string |  |
| `limit` | number |  |
| `links.first` | string |  |
| `links.last` | string |  |
| `links.next` | string |  |
| `links.prev` | string |  |
| `links.self` | string |  |
| `offset` | number |  |
| `size` | number |  |
| `total` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Miro API, this operation is `GET /boards` (base URL `https://api.miro.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-boards.md) for the provider-specific parameters and requirements.

