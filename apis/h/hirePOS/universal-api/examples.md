# HirePOS Universal API Examples

These examples use the MindCloud API key and HirePOS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Authenticate

Validates API credentials for a HirePOS account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/authenticate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/authenticate?${params}`, {
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
      "businessCode": "string",
      "businessName": "Ava Chen",
      "errorMessage": "string",
      "errorRaised": "string",
      "errorType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Authenticate action reference](actions/authenticate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hirePOS/latest/actions/authenticate).

## Create Customer

Creates a new customer in HirePOS.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/create-customer', {
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
      "customers": [
        {}
      ],
      "errorMessage": "string",
      "errorRaised": "string",
      "errorType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hirePOS/latest/actions/create-customer).
