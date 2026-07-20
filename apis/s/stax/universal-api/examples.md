# Stax Universal API Examples

These examples use the MindCloud API key and Stax connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers

Retrieves customers from Stax.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-customers?${params}`, {
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
      "address1": "string",
      "address2": "string",
      "addressCity": "string",
      "addressState": "string",
      "addressZip": "string",
      "company": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": "string",
      "lastname": "Chen",
      "phone": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stax/latest/actions/list-customers).

## Capture Pre-Auth Transaction

Captures a pre-authorized transaction in Stax.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stax/latest/actions/capture-pre-auth-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stax/latest/actions/capture-pre-auth-transaction', {
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
      "createdAt": "string",
      "currency": "string",
      "customerId": "string",
      "id": "string",
      "isRefundable": true,
      "isVoidable": true,
      "paymentMethodId": "string",
      "success": true,
      "total": 1,
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Capture Pre-Auth Transaction action reference](actions/capture-pre-auth-transaction.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stax/latest/actions/capture-pre-auth-transaction).
