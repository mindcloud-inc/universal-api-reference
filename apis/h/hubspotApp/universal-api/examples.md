# HubSpot Universal API Examples

These examples use the MindCloud API key and HubSpot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves contacts from HubSpot.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-contacts?${params}`, {
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
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "properties": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hubspotApp/latest/actions/list-contacts).

## Add User

Creates a new user in HubSpot.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/add-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "sendWelcomeEmail": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/add-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "sendWelcomeEmail": true
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
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "primaryTeamId": "string",
      "roleIds": [
        "string"
      ],
      "secondaryTeamIds": [
        "string"
      ],
      "superAdmin": true
    }
  ],
  "meta": {}
}
```

See the full [Add User action reference](actions/add-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hubspotApp/latest/actions/add-user).
