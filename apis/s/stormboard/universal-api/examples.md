# Stormboard Universal API Examples

These examples use the MindCloud API key and Stormboard connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Authentication

Checks whether your Stormboard authentication token is valid.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/check-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/check-authentication?${params}`, {
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
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Check Authentication action reference](actions/check-authentication.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stormboard/latest/actions/check-authentication).

## Accept Storm Invite

Accepts a Storm invite in Stormboard.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/accept-storm-invite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stormId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/accept-storm-invite', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stormId": 1
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
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Accept Storm Invite action reference](actions/accept-storm-invite.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stormboard/latest/actions/accept-storm-invite).
