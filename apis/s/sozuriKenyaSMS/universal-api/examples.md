# Sozuri (Kenya) SMS Universal API Examples

These examples use the MindCloud API key and Sozuri (Kenya) SMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves contacts from Sozuri.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/list-contacts?${params}`, {
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
      "contacts": {},
      "group": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sozuriKenyaSMS/latest/actions/list-contacts).

## Create Contacts

Creates one or more contacts in Sozuri.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/create-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/create-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts[]": [{}]
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Contacts action reference](actions/create-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sozuriKenyaSMS/latest/actions/create-contacts).
