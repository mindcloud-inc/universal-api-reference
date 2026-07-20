# CoachAccountable Universal API Examples

These examples use the MindCloud API key and CoachAccountable connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Profile

Retrieves an account profile from CoachAccountable.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/get-account-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/get-account-profile?${params}`, {
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
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Profile action reference](actions/get-account-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/coachAccountable/latest/actions/get-account-profile).

## Activate Client

Activates a client in CoachAccountable.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/activate-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/activate-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": 1
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Activate Client action reference](actions/activate-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/coachAccountable/latest/actions/activate-client).
