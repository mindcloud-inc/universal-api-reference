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

## Verify Webhook Endpoint



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ramp/latest/actions/new-action1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "challenge": "string",
  "webhookId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ramp/latest/actions/new-action1', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "challenge": "string",
    "webhookId": "string"
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

See the full [Verify Webhook Endpoint action reference](actions/new-action1.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ramp/latest/actions/new-action1).
