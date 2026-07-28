# Ramp Universal API Examples

These examples use the MindCloud API key and Ramp connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Vendors



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ramp/latest/actions/list-vendors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ramp/latest/actions/list-vendors?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Vendors action reference](actions/list-vendors.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ramp/latest/actions/list-vendors).

## Upload a new memo for a transaction



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ramp/latest/actions/upload-transaction-memo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "memo": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ramp/latest/actions/upload-transaction-memo', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "memo": "string"
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
      "id": "string",
      "memo": "string"
    }
  ],
  "meta": {}
}
```

See the full [Upload a new memo for a transaction action reference](actions/upload-transaction-memo.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ramp/latest/actions/upload-transaction-memo).
