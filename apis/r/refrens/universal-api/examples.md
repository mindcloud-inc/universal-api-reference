# Refrens Universal API Examples

These examples use the MindCloud API key and Refrens connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Token



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/refrens/latest/actions/validate-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/refrens/latest/actions/validate-token?${params}`, {
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
      "accessToken": "string",
      "appId": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Validate Token action reference](actions/validate-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/refrens/latest/actions/validate-token).

## Add Invoice Payment



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/refrens/latest/actions/add-invoice-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoice": "string",
  "amount": 1,
  "paymentDate": "2026-05-07T12:00:00.000Z",
  "paymentMethod": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/refrens/latest/actions/add-invoice-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoice": "string",
    "amount": 1,
    "paymentDate": "2026-05-07T12:00:00.000Z",
    "paymentMethod": "string"
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
      "_id": "string",
      "amount": 1,
      "appId": "string",
      "business": "string",
      "isApproved": true,
      "isRemoved": true,
      "notes": "string",
      "payerBusiness": "string",
      "paymentDate": "2026-05-07T12:00:00.000Z",
      "paymentMethod": "string",
      "tds": 1,
      "transactionCharge": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Invoice Payment action reference](actions/add-invoice-payment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/refrens/latest/actions/add-invoice-payment).
