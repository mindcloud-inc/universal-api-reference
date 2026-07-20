# eSign Genie Universal API Examples

These examples use the MindCloud API key and eSign Genie connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List All Users

Retrieves users from eSign Genie.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/list-users?${params}`, {
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
      "allActiveUsers": 1,
      "allInactiveUsers": 1,
      "usersList": [
        {
          "active": true,
          "emailId": "ava@example.com",
          "firstName": "Ava",
          "lastName": "Chen",
          "partyId": 1,
          "userRole": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List All Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eSignGenie/latest/actions/list-users).

## Cancel Envelope

Cancels an envelope in eSign Genie.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/cancel-envelope" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/cancel-envelope', {
  method: 'PUT',
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
  "data": [],
  "meta": {}
}
```

See the full [Cancel Envelope action reference](actions/cancel-envelope.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eSignGenie/latest/actions/cancel-envelope).
