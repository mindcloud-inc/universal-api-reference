# Conexteo Universal API Examples

These examples use the MindCloud API key and Conexteo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contact Lists

Finds contact lists in Conexteo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/list-contact-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/list-contact-lists?${params}`, {
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
      "contacts_count": 1,
      "id": 1,
      "name": "Ava Chen",
      "rcsCapabilityStatus": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Contact Lists action reference](actions/list-contact-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/conexteo/latest/actions/list-contact-lists).

## Add Contacts

Creates contacts in Conexteo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/add-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactlist_id": 1,
  "contacts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/add-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactlist_id": 1,
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
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Contacts action reference](actions/add-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/conexteo/latest/actions/add-contacts).
