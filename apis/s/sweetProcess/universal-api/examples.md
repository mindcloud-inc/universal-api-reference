# SweetProcess Universal API Examples

These examples use the MindCloud API key and SweetProcess connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Procedures

Retrieves procedures from SweetProcess.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/list-procedures?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/list-procedures?${params}`, {
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
      "accountId": 1,
      "approvedAt": "2026-05-07T12:00:00.000Z",
      "approvedBy": {},
      "author": {},
      "canAssign": true,
      "canChange": true,
      "canDelete": true,
      "canEdit": true,
      "canExport": true,
      "connections": [
        {}
      ],
      "content": "string",
      "contentType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currentVersion": {},
      "description": {},
      "diagramPngStatus": "string",
      "diagramPngUrl": "https://example.com",
      "editedAt": "2026-05-07T12:00:00.000Z",
      "embedUrl": "https://example.com",
      "hashid": "string",
      "htmlUrl": "https://example.com",
      "id": 1,
      "isLarge": true,
      "lanes": {},
      "lastReviewAt": "2026-05-07T12:00:00.000Z",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "nextReviewAt": "2026-05-07T12:00:00.000Z",
      "originalAuthor": {},
      "policies": [
        {}
      ],
      "private": true,
      "processes": [
        {}
      ],
      "reviewer": {},
      "reviewPeriodMonths": 1,
      "signoffRequestedAt": "2026-05-07T12:00:00.000Z",
      "signoffRequestedBy": {},
      "slug": "string",
      "stepsBlockedAt": "2026-05-07T12:00:00.000Z",
      "tags": [
        "string"
      ],
      "teamMemberships": [
        {}
      ],
      "teamNames": [
        "Ava Chen"
      ],
      "templateAt": "2026-05-07T12:00:00.000Z",
      "thumbnail": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Procedures action reference](actions/list-procedures.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sweetProcess/latest/actions/list-procedures).

## Create Invitation

Creates a new invitation in SweetProcess.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/create-invitation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invitations[].contentType": "team",
  "invitations[].permission": "view",
  "invitations[].objectId": 1,
  "invitations[].toUserId": "https://www.sweetprocess.com/api/v1/users/32010/"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/create-invitation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invitations[].contentType": "team",
    "invitations[].permission": "view",
    "invitations[].objectId": 1,
    "invitations[].toUserId": "https://www.sweetprocess.com/api/v1/users/32010/"
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
      "contentType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fromUser": {},
      "id": 1,
      "objectId": 1,
      "permission": "string",
      "sharedItem": {},
      "status": "string",
      "toUser": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Invitation action reference](actions/create-invitation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sweetProcess/latest/actions/create-invitation).
