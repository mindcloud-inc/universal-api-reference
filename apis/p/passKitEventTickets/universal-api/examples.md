# PassKit Event Tickets Universal API Examples

These examples use the MindCloud API key and PassKit Event Tickets connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Profile

Retrieves your user profile from PassKit.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/get-user-profile?${params}`, {
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
      "companyId": "string",
      "companyName": "Ava Chen",
      "companyStatus": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "expiresAt": "string",
      "regionId": "string",
      "userId": "string",
      "username": "Ava Chen",
      "userPermissions": "string",
      "userStatus": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User Profile action reference](actions/get-user-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/passKitEventTickets/latest/actions/get-user-profile).

## Copy Production

Creates a copy of a production in PassKit.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/copy-production" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/copy-production', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Copy Production action reference](actions/copy-production.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/passKitEventTickets/latest/actions/copy-production).
