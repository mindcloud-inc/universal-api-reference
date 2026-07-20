# Selock Universal API Examples

These examples use the MindCloud API key and Selock connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Token



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selock/latest/actions/verify-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selock/latest/actions/verify-token?${params}`, {
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
      "res": true
    }
  ],
  "meta": {}
}
```

See the full [Verify Token action reference](actions/verify-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/selock/latest/actions/verify-token).

## Change Lock Status



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/selock/latest/actions/change-lock-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "status": "string",
  "lock_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/selock/latest/actions/change-lock-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "status": "string",
    "lock_id": "string"
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
      "res": true
    }
  ],
  "meta": {}
}
```

See the full [Change Lock Status action reference](actions/change-lock-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/selock/latest/actions/change-lock-status).
