# Insightly Universal API Examples

These examples use the MindCloud API key and Insightly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves a list of contacts from Insightly.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightly/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightly/latest/actions/list-contacts?${params}`, {
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
      "contactId": 1,
      "createdUserId": 1,
      "dateCreatedUtc": "2026-05-07T12:00:00.000Z",
      "dateUpdatedUtc": "2026-05-07T12:00:00.000Z",
      "emailAddress": "ava@example.com",
      "emailOptedOut": true,
      "firstName": "Ava",
      "imageUrl": "https://example.com",
      "lastActivityDateUtc": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "nextActivityDateUtc": "2026-05-07T12:00:00.000Z",
      "organisationId": 1,
      "ownerUserId": 1,
      "phone": "string",
      "title": "string",
      "visibleTo": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/insightly/latest/actions/list-contacts).

## Create Contact

Creates a new contact in Insightly.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/insightly/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightly/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava"
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
      "createdUserId": 1,
      "dateCreatedUtc": "2026-05-07T12:00:00.000Z",
      "dateUpdatedUtc": "2026-05-07T12:00:00.000Z",
      "emailAddress": "ava@example.com",
      "emailOptedOut": true,
      "firstName": "Ava",
      "imageUrl": "https://example.com",
      "lastActivityDateUtc": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "nextActivityDateUtc": "2026-05-07T12:00:00.000Z",
      "organisationId": 1,
      "ownerUserId": 1,
      "phone": "string",
      "title": "string",
      "visibleTo": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/insightly/latest/actions/create-contact).
