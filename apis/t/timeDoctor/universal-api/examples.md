# Time Doctor Universal API Examples

These examples use the MindCloud API key and Time Doctor connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authorization

Retrieves authorization details from Time Doctor.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-authorization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-authorization?${params}`, {
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
      "active": true,
      "adminSettings": {},
      "companies": [
        {}
      ],
      "email": "ava@example.com",
      "emailConfirmed": true,
      "id": "string",
      "lastSeenGlobal": {},
      "lastTrackGlobal": {},
      "name": "Ava Chen",
      "timezones": "string",
      "twoFactorAuth": true
    }
  ],
  "meta": {}
}
```

See the full [Get Authorization action reference](actions/get-authorization.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timeDoctor/latest/actions/get-authorization).

## Create Project

Creates a new project in Time Doctor.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/create-project', {
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
      "creatorId": "string",
      "deleted": true,
      "description": "string",
      "id": "string",
      "integration": {},
      "name": "Ava Chen",
      "scope": "string",
      "weight": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Project action reference](actions/create-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timeDoctor/latest/actions/create-project).
