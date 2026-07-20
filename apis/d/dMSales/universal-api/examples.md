# DMSales Universal API Examples

These examples use the MindCloud API key and DMSales connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from DMSales.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/get-current-user?${params}`, {
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
      "company_name": "Ava Chen",
      "email": "ava@example.com",
      "name": "Ava",
      "surname": "Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dMSales/latest/actions/get-current-user).

## Add Contact Note

Creates a contact note in DMSales.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/add-contact-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "baseKey": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/add-contact-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "baseKey": "string",
    "content": "string"
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
      "message": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Contact Note action reference](actions/add-contact-note.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dMSales/latest/actions/add-contact-note).
