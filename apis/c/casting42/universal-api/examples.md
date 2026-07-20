# Casting42 Universal API Examples

These examples use the MindCloud API key and Casting42 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Talents

Retrieves all talent records from Casting42.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/casting42/latest/actions/list-talents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/casting42/latest/actions/list-talents?${params}`, {
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
      "age": 1,
      "birthday": "string",
      "createdAt": "string",
      "customFields": [
        {}
      ],
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "hiddenName": "Ava Chen",
      "id": "string",
      "lastName": "Chen",
      "mobilePhone": "string",
      "profilePicture": "string",
      "skills": {},
      "slug": "string",
      "stageName": "Ava Chen",
      "tag": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Talents action reference](actions/list-talents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/casting42/latest/actions/list-talents).

## Authenticate

Creates a Casting42 authentication token from your API key.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/casting42/latest/actions/authenticate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/casting42/latest/actions/authenticate', {
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
      "accessToken": "string",
      "authenticated": true,
      "expiresIn": 1,
      "expiresOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Authenticate action reference](actions/authenticate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/casting42/latest/actions/authenticate).
