# Escrow.com Universal API Examples

These examples use the MindCloud API key and Escrow.com connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Customer

Retrieves current customer details from Escrow.com.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-current-customer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-current-customer?${params}`, {
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
      "accountType": "string",
      "company": {},
      "customerEmailVerification": {},
      "electronicVerification": {},
      "email": "ava@example.com",
      "id": 1,
      "verification": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Current Customer action reference](actions/get-current-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/escrowcom/latest/actions/get-current-customer).

## Create Customer

Creates a new customer in Escrow.com.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen"
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
      "accountType": "string",
      "address": {},
      "company": {},
      "customerEmailVerification": {},
      "displayName": "Ava Chen",
      "electronicVerification": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "phoneNumber": "string",
      "verification": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/escrowcom/latest/actions/create-customer).
