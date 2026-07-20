# echowin Universal API Examples

These examples use the MindCloud API key and echowin connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves contacts from echowin.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/echowin/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/echowin/latest/actions/list-contacts?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/echowin/latest/actions/list-contacts).

## Add Contact Assignments

Adds contact assignments in echowin.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/echowin/latest/actions/add-contact-assignments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "userIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/echowin/latest/actions/add-contact-assignments', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "userIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Contact Assignments action reference](actions/add-contact-assignments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/echowin/latest/actions/add-contact-assignments).
