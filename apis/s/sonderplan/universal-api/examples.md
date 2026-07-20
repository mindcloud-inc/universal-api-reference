# Sonderplan Universal API Examples

These examples use the MindCloud API key and Sonderplan connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Instance



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-instance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-instance?${params}`, {
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
      "created": 1,
      "createdId": 1,
      "domain": "string",
      "name": "Ava Chen",
      "updated": 1,
      "updatedId": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Instance action reference](actions/get-instance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sonderplan/latest/actions/get-instance).

## Bulk Bookings



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/bulk-bookings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/bulk-bookings', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {}
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
      "delete": {},
      "save": {}
    }
  ],
  "meta": {}
}
```

See the full [Bulk Bookings action reference](actions/bulk-bookings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sonderplan/latest/actions/bulk-bookings).
