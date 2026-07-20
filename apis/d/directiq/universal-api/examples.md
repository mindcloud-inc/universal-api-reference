# DirectIQ Universal API Examples

These examples use the MindCloud API key and DirectIQ connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves a paginated list of contacts from DirectIQ.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-contacts?${params}`, {
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
      "clientId": 1,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "keys": [
        [
          {}
        ]
      ],
      "lastName": "Chen",
      "lists": [
        [
          {}
        ]
      ],
      "notes": [
        [
          {}
        ]
      ],
      "quality": 1,
      "reactivationRequests": [
        [
          {}
        ]
      ],
      "status": "string",
      "statusDate": "2026-05-07T12:00:00.000Z",
      "tags": [
        [
          {}
        ]
      ],
      "updatedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/directiq/latest/actions/list-contacts).

## Add a contact to a list

Adds a contact to a list in DirectIQ.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/add-a-contact-to-a-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/directiq/latest/actions/add-a-contact-to-a-list', {
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
  "data": [],
  "meta": {}
}
```

See the full [Add a contact to a list action reference](actions/add-a-contact-to-a-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/directiq/latest/actions/add-a-contact-to-a-list).
