# Flexmail Universal API Examples

These examples use the MindCloud API key and Flexmail connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves contact records from your Flexmail account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/list-contacts?${params}`, {
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
      "custom_fields": {},
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "language": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flexmail/latest/actions/list-contacts).

## Add Contact Import Records

Adds records to a contact import in Flexmail.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/add-contact-import-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "records[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/add-contact-import-records', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "records[]": [{}]
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Contact Import Records action reference](actions/add-contact-import-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flexmail/latest/actions/add-contact-import-records).
