# GorillaDesk Universal API Examples

These examples use the MindCloud API key and GorillaDesk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Company

Retrieves company details from GorillaDesk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/retrieve-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/retrieve-company?${params}`, {
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
      "address": "string",
      "city": "string",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "officeHours": {
        "end": "string",
        "start": "string"
      },
      "phone": "string",
      "state": "string",
      "timezone": "string",
      "website": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Company action reference](actions/retrieve-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gorillaDesk/latest/actions/retrieve-company).

## Create Customer

Creates a new customer in GorillaDesk.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "location": {},
  "location.addressLine1": "string",
  "location.city": "string",
  "location.state": "string",
  "location.zip": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "location": {},
    "location.addressLine1": "string",
    "location.city": "string",
    "location.state": "string",
    "location.zip": "string"
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gorillaDesk/latest/actions/create-customer).
