# Quantum Digital Universal API Examples

These examples use the MindCloud API key and Quantum Digital connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Orders



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/list-orders?${params}`, {
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
      "orders": [
        {}
      ],
      "paging": {},
      "rowEnd": 1,
      "rowStart": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

See the full [List Orders action reference](actions/list-orders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quantumDigital/latest/actions/list-orders).

## Create Payment Method



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/create-payment-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "billingAddress1": "string",
  "billingCity": "string",
  "billingCountry": "Canada",
  "billingPostalCode": "string",
  "billingStateProvince": "string",
  "creditCardNumber": "string",
  "creditCardType": "American Express",
  "expMonth": "string",
  "expYear": "string",
  "nameOnCard": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/create-payment-method', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "billingAddress1": "string",
    "billingCity": "string",
    "billingCountry": "Canada",
    "billingPostalCode": "string",
    "billingStateProvince": "string",
    "creditCardNumber": "string",
    "creditCardType": "American Express",
    "expMonth": "string",
    "expYear": "string",
    "nameOnCard": "Ava Chen"
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Payment Method action reference](actions/create-payment-method.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quantumDigital/latest/actions/create-payment-method).
