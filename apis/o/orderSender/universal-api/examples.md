# Order Sender Universal API Examples

These examples use the MindCloud API key and Order Sender connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Connection

Retrieves Order Sender account status and API access validity.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/verify-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/verify-connection?${params}`, {
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
      "account": "string",
      "expire": "2026-05-07T12:00:00.000Z",
      "msg": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Verify Connection action reference](actions/verify-connection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/orderSender/latest/actions/verify-connection).

## Import Commissions

Imports commission records into Order Sender.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/import-commissions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/import-commissions', {
  method: 'POST',
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
      "msg": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Import Commissions action reference](actions/import-commissions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/orderSender/latest/actions/import-commissions).
