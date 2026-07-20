# lc.cx Universal API Examples

These examples use the MindCloud API key and lc.cx connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves account details from lc.cx.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lccx/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lccx/latest/actions/get-account?${params}`, {
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
      "max_shortlinks": 1,
      "plan": "string",
      "reset_date": "2026-05-07T12:00:00.000Z",
      "shortlinks_usage": 1,
      "tags": true,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lccx/latest/actions/get-account).

## Create Short Link

Creates a new short link in lc.cx.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lccx/latest/actions/create-short-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destination": "string",
  "domainId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lccx/latest/actions/create-short-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destination": "string",
    "domainId": "string"
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

See the full [Create Short Link action reference](actions/create-short-link.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lccx/latest/actions/create-short-link).
