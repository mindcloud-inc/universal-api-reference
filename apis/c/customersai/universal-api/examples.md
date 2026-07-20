# Customers.ai Universal API Examples

These examples use the MindCloud API key and Customers.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contact IDs



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customersai/latest/actions/list-contact-ids?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customersai/latest/actions/list-contact-ids?${params}`, {
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
      "ids": [
        1
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Contact IDs action reference](actions/list-contact-ids.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/customersai/latest/actions/list-contact-ids).

## Create Contact

Creates an SMS contact in Customers.ai, or updates an existing match.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customersai/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customersai/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phone": "string"
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
      "contactId": 1,
      "recipientId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/customersai/latest/actions/create-contact).
