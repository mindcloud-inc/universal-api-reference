# Pachca (Admin) Universal API Examples

These examples use the MindCloud API key and Pachca (Admin) connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Profile

Retrieves your profile from the Pachca Admin API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/get-profile?${params}`, {
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
      "data": {
        "bot": true,
        "createdAt": "string",
        "department": {},
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": 1,
        "imageUrl": {},
        "inviteStatus": "string",
        "lastActivityAt": "string",
        "lastName": "Chen",
        "nickname": "Ava Chen",
        "phoneNumber": {},
        "role": "string",
        "sso": true,
        "suspended": true,
        "timeZone": "string",
        "title": {},
        "userStatus": {}
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Profile action reference](actions/get-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pachcaAdmin/latest/actions/get-profile).

## Add Chat Group Tags



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/add-chat-group-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupTagIds[]": [
    1
  ],
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/add-chat-group-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupTagIds[]": [1],
    "id": 1
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
      "data": {}
    }
  ],
  "meta": {}
}
```

See the full [Add Chat Group Tags action reference](actions/add-chat-group-tags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pachcaAdmin/latest/actions/add-chat-group-tags).
