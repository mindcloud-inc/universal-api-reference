# Quiltt Universal API Examples

These examples use the MindCloud API key and Quiltt connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Profiles



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/list-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/list-profiles?${params}`, {
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
      "address": {},
      "at": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dateOfBirth": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "names": {},
      "phone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Profiles action reference](actions/list-profiles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quiltt/latest/actions/list-profiles).

## Create Profile



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/create-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/create-profile', {
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
      "address": {},
      "at": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dateOfBirth": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "names": {},
      "phone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Profile action reference](actions/create-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quiltt/latest/actions/create-profile).
