# VentiPay Universal API Examples

These examples use the MindCloud API key and VentiPay connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Balance

Retrieves the current merchant balance from VentiPay.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ventiPay/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ventiPay/latest/actions/get-balance?${params}`, {
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

See the full [Get Balance action reference](actions/get-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ventiPay/latest/actions/get-balance).

## Create Customer

Creates a new customer in VentiPay.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ventiPay/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "country": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ventiPay/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "country": "string"
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
      "bnpl_credit_currency": "string",
      "bnpl_credit_limit": 1,
      "country": "string",
      "created_at": "string",
      "disabled": true,
      "email": "ava@example.com",
      "email_validated": true,
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "object": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ventiPay/latest/actions/create-customer).
