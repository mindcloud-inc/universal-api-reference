# Scoro Universal API Examples

These examples use the MindCloud API key and Scoro connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves contacts from Scoro.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-contacts?${params}`, {
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
      "addresses": {},
      "bankaccount": "string",
      "birthday": {},
      "cat_id": 1,
      "client_profile_id": 1,
      "comments": "string",
      "contact_id": 1,
      "contact_picture": "string",
      "contact_type": "string",
      "created_date": "string",
      "deleted_date": {},
      "id_code": "string",
      "is_client": true,
      "is_deleted": true,
      "is_supplier": true,
      "lastname": "Chen",
      "manager_email": "ava@example.com",
      "manager_id": 1,
      "means_of_contact": {},
      "modified_date": "string",
      "name": "Ava Chen",
      "permissions": {},
      "position": "string",
      "reference_no": "string",
      "search_name": "Ava Chen",
      "sex": "string",
      "timezone": "string",
      "vatno": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scoro/latest/actions/list-contacts).

## Update Calendar Event

Updates an existing calendar event in Scoro.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/update-calendar-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scoro/latest/actions/update-calendar-event', {
  method: 'PUT',
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
      "data": {},
      "messages": {},
      "status": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

See the full [Update Calendar Event action reference](actions/update-calendar-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scoro/latest/actions/update-calendar-event).
