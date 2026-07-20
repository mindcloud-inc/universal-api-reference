# Mendato Universal API Examples

These examples use the MindCloud API key and Mendato connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-company?${params}`, {
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
      "company": {
        "companyName": "Ava Chen",
        "email": "ava@example.com",
        "id": "string",
        "phone": "string",
        "vatId": "string",
        "website": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Company action reference](actions/get-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mendato/latest/actions/get-company).

## Create Customer



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mendato/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables": {}
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
      "createCustomer": {
        "customer": {
          "addressSupplement": "string",
          "companyName": "Ava Chen",
          "firstName": "Ava",
          "id": "string",
          "lastName": "Chen",
          "number": 1,
          "salutation": "string",
          "type": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mendato/latest/actions/create-customer).
