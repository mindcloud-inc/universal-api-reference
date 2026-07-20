# Starfish Universal API Examples

These examples use the MindCloud API key and Starfish connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current authenticated user from Starfish.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starfish/latest/actions/get-current-user?${params}`, {
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
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "id": 1,
      "meta": {},
      "rights": [
        "string"
      ],
      "status": 1,
      "type": "string",
      "userRegistered": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/starfish/latest/actions/get-current-user).

## Create Accommodation

Creates a new accommodation in Starfish.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/create-accommodation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starfish/latest/actions/create-accommodation', {
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
      "accommodationId": 1,
      "accommodationUid": "string",
      "adminId": 1,
      "arrangements": [
        {}
      ],
      "description": "string",
      "id": 1,
      "labels": [
        {}
      ],
      "media": [
        {}
      ],
      "meta": {},
      "name": "Ava Chen",
      "rank": 1,
      "services": [
        {}
      ],
      "status": "string",
      "translations": [
        {}
      ],
      "type": "string",
      "vatProcent": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Accommodation action reference](actions/create-accommodation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/starfish/latest/actions/create-accommodation).
