# Rithum DSCO Universal API Examples

These examples use the MindCloud API key and Rithum DSCO connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test Connection

Retrieves a hello-world response from Rithum DSCO.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/test-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/test-connection?${params}`, {
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
      "hello": "string"
    }
  ],
  "meta": {}
}
```

See the full [Test Connection action reference](actions/test-connection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rithumDSCOV2/latest/actions/test-connection).

## Acknowledge Order Items

Acknowledges order items in Rithum DSCO.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/acknowledge-order-items" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/acknowledge-order-items', {
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
  "data": [
    {
      "requestId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Acknowledge Order Items action reference](actions/acknowledge-order-items.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rithumDSCOV2/latest/actions/acknowledge-order-items).
