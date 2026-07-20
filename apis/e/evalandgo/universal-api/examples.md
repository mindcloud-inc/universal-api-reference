# Evalandgo Universal API Examples

These examples use the MindCloud API key and Evalandgo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Groups

Retrieves groups from Evalandgo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/list-groups?${params}`, {
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
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "hydra:member": [
        {
          "@id": "string",
          "@type": "string",
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "hydra:totalItems": 1
    }
  ],
  "meta": {}
}
```

See the full [List Groups action reference](actions/list-groups.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/evalandgo/latest/actions/list-groups).

## Create Contact

Creates a new contact in Evalandgo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/create-contact', {
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
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "createAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "hasPassword": true,
      "id": 1,
      "lastName": "Chen",
      "optinAt": "string",
      "phone": "string",
      "status": {},
      "username": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/evalandgo/latest/actions/create-contact).
