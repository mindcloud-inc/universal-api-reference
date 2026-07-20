# Mighty Networks Universal API Examples

These examples use the MindCloud API key and Mighty Networks connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Mighty Networks.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/get-current-user?connectionId=$CONNECTION_ID&networkId=%7B%7Bcredentials.networkId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "networkId": "{{credentials.networkId}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/get-current-user?${params}`, {
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
      "network": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "id": 1,
        "purpose": "string",
        "subdomain": "string",
        "subtitle": "string",
        "title": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "user": {
        "admin": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen",
        "shortBio": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mightyNetworks/latest/actions/get-current-user).

## Add Space Member

Adds a member to a space in Mighty Networks.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/add-space-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "networkId": "{{credentials.networkId}}",
  "spaceId": "23049325",
  "userId": "38689843"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/add-space-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "networkId": "{{credentials.networkId}}",
    "spaceId": "23049325",
    "userId": "38689843"
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
      "ambassadorLevel": "string",
      "avatar": "string",
      "bio": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "location": "string",
      "permalink": "https://example.com",
      "referralCount": 1,
      "timeZone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Space Member action reference](actions/add-space-member.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mightyNetworks/latest/actions/add-space-member).
