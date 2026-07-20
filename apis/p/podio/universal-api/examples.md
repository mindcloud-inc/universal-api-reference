# Podio Universal API Examples

These examples use the MindCloud API key and Podio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Status

Retrieves user status details from Podio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-user-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-user-status?${params}`, {
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
      "betas": [
        "string"
      ],
      "calendarCode": "string",
      "flags": [
        "string"
      ],
      "inbox": {},
      "inboxNew": 1,
      "mailbox": {},
      "messageUnreadCount": 1,
      "presence": {},
      "profile": {},
      "properties": {},
      "push": {},
      "referral": {},
      "user": {}
    }
  ],
  "meta": {}
}
```

See the full [Get User Status action reference](actions/get-user-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/podio/latest/actions/get-user-status).

## Add Comment to Object

Creates a comment on a Podio object.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/podio/latest/actions/add-comment-to-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "item",
  "id": "12345",
  "value": "Please review the updated timeline."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/podio/latest/actions/add-comment-to-object', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "item",
    "id": "12345",
    "value": "Please review the updated timeline."
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
      "commentId": 1,
      "createdBy": {},
      "createdOn": "2026-05-07T12:00:00.000Z",
      "createdVia": {},
      "embed": {},
      "embedFile": {},
      "externalId": "string",
      "files": [
        {}
      ],
      "grantedUsers": [
        {}
      ],
      "invitedUsers": [
        {}
      ],
      "isLiked": true,
      "lastEditOn": "2026-05-07T12:00:00.000Z",
      "likeCount": 1,
      "questions": [
        {}
      ],
      "ref": {},
      "richValue": "string",
      "rights": [
        "string"
      ],
      "user": {},
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Comment to Object action reference](actions/add-comment-to-object.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/podio/latest/actions/add-comment-to-object).
