# KEYZY Universal API Examples

These examples use the MindCloud API key and KEYZY connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Status Check

Retrieves the current API server status from KEYZY.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/get-status-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/get-status-check?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Status Check action reference](actions/get-status-check.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kEYZY/latest/actions/get-status-check).

## Register License

Registers a new customer to a KEYZY license.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/register-license" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "name": "Ava Chen",
  "skuNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/register-license', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "name": "Ava Chen",
    "skuNumber": "string"
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
      "message": {
        "serial": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Register License action reference](actions/register-license.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kEYZY/latest/actions/register-license).
