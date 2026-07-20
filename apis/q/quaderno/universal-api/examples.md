# Quaderno Universal API Examples

These examples use the MindCloud API key and Quaderno connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tax Codes

Retrieves supported tax codes from Quaderno.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/list-tax-codes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/list-tax-codes?${params}`, {
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
      "description": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Tax Codes action reference](actions/list-tax-codes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quaderno/latest/actions/list-tax-codes).

## Create Contact

Creates a new contact in Quaderno.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava"
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
      "city": {},
      "country": "string",
      "createdAt": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": 1,
      "kind": "string",
      "language": "string",
      "lastName": {},
      "notes": {},
      "permalink": "https://example.com",
      "phone1": {},
      "postalCode": {},
      "processor": {},
      "processorId": {},
      "region": {},
      "streetLine1": {},
      "streetLine2": {},
      "taxId": {},
      "taxStatus": "string",
      "web": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quaderno/latest/actions/create-contact).
