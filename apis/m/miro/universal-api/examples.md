# Miro Universal API Examples

These examples use the MindCloud API key and Miro connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Access Token Context

Retrieves access token context from Miro.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/miro/latest/actions/get-access-token-context?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/miro/latest/actions/get-access-token-context?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "createdBy": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "organization": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "scopes": [
        "string"
      ],
      "team": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "type": "string",
      "user": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Access Token Context action reference](actions/get-access-token-context.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/miro/latest/actions/get-access-token-context).

## Create Board

Creates a new board in Miro.

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

Example response:

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

See the full [Create Board action reference](actions/create-board.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/miro/latest/actions/create-board).
