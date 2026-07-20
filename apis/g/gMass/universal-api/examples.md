# GMass Universal API Examples

These examples use the MindCloud API key and GMass connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User

Retrieves your current GMass account information.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gMass/latest/actions/get-user?${params}`, {
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
      "emailAddress": "ava@example.com",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get User action reference](actions/get-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gMass/latest/actions/get-user).

## Add Account Unsubscribe

Adds an address to your GMass unsubscribe list.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/add-account-unsubscribe" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailAddress": "gmass-stage3@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gMass/latest/actions/add-account-unsubscribe', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailAddress": "gmass-stage3@example.com"
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
      "emailAddress": "ava@example.com",
      "sender": "string",
      "unsubscribeTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Account Unsubscribe action reference](actions/add-account-unsubscribe.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gMass/latest/actions/add-account-unsubscribe).
