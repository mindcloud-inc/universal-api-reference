# Novofon Universal API Examples

These examples use the MindCloud API key and Novofon connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Balance

Retrieves account balance from Novofon.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/novofon/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/novofon/latest/actions/get-balance?${params}`, {
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
      "balance": 1,
      "currency": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Balance action reference](actions/get-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/novofon/latest/actions/get-balance).

## Request Callback

Creates a callback request in Novofon.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/novofon/latest/actions/request-callback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/novofon/latest/actions/request-callback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "to": "string"
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

See the full [Request Callback action reference](actions/request-callback.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/novofon/latest/actions/request-callback).
