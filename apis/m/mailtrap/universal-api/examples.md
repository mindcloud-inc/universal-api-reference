# Mailtrap Universal API Examples

These examples use the MindCloud API key and Mailtrap connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Permissions



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/list-permissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/list-permissions?${params}`, {
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

See the full [List Permissions action reference](actions/list-permissions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailtrap/latest/actions/list-permissions).

## Create Contact

Creates a new contact in Mailtrap.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/create-contact', {
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
      "data": {
        "createdAt": 1,
        "email": "ava@example.com",
        "fields": {
          "company": "string",
          "firstName": "Ava",
          "lastName": "Chen"
        },
        "id": "string",
        "listIds": [
          1
        ],
        "status": "string",
        "updatedAt": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailtrap/latest/actions/create-contact).
