# Faithlife Universal API Examples

These examples use the MindCloud API key and Faithlife connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Faithlife.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/get-current-user?${params}`, {
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
      "alias": "string",
      "avatarUrls": {},
      "dayPhone": "string",
      "email": "ava@example.com",
      "gender": "string",
      "id": "string",
      "isSolicitable": true,
      "name": "Ava Chen",
      "token": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/faithlife/latest/actions/get-current-user).

## Accept Invite To Group

Accepts a group invite in Faithlife.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/accept-invite-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inviteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/accept-invite-to-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inviteId": "string"
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
      "membershipId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Accept Invite To Group action reference](actions/accept-invite-to-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/faithlife/latest/actions/accept-invite-to-group).
