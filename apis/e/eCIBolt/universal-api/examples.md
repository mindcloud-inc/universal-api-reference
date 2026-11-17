# ECI Bolt Universal API Examples

These examples use the MindCloud API key and ECI Bolt connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Stages



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-stages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-stages?${params}`, {
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
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [List Stages action reference](actions/list-stages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eCIBolt/latest/actions/list-stages).

## Create Customer



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/create-customer', {
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
      "billingAddress": {
        "address1": "string",
        "address2": "string",
        "city": "string",
        "state": "string",
        "zip": "string"
      },
      "billingContact": {
        "cellphone": "string",
        "email": "ava@example.com",
        "fax": "string",
        "fullname": "Ava Chen",
        "phone": "string"
      },
      "corporateAddress": {
        "address1": "string",
        "address2": "string",
        "city": "string",
        "state": "string",
        "zip": "string"
      },
      "corporateContact": {
        "cellphone": "string",
        "email": "ava@example.com",
        "fax": "string",
        "fullname": "Ava Chen",
        "phone": "string"
      },
      "email": "ava@example.com",
      "emailConfirmationToSupervisor": true,
      "externalId": "string",
      "id": 1,
      "name": "Ava Chen",
      "notes": "string",
      "optOutAutoConfirmation": true,
      "optOutEmailConfirmation": true,
      "phone": "string",
      "poRequired": true,
      "status": "string",
      "supervisor": "string",
      "workOrderNotes": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eCIBolt/latest/actions/create-customer).
