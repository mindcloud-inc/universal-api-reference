# PhoneBurner Universal API Examples

These examples use the MindCloud API key and PhoneBurner connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves a list of contacts from PhoneBurner.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phoneBurner/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phoneBurner/latest/actions/list-contacts?${params}`, {
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
      "archived": "string",
      "category": {},
      "contactOwnerId": "string",
      "contactUserId": "string",
      "dateAdded": "string",
      "dateUpdated": "string",
      "description": "string",
      "firstName": "Ava",
      "lastName": "Chen",
      "locationName": "Ava Chen",
      "notes": {},
      "ownerId": "string",
      "primaryEmail": {},
      "primaryPhone": {},
      "rawPhone": "string",
      "region": "string",
      "removed": "string",
      "timeZone": "string",
      "totalCalls": "string",
      "trashed": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/phoneBurner/latest/actions/list-contacts).

## Create Contact

Creates a new contact in PhoneBurner.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/phoneBurner/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/phoneBurner/latest/actions/create-contact', {
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
      "contactUserId": "string",
      "dateAdded": "string",
      "emailAddress": "ava@example.com",
      "externalCrmData": [
        {}
      ],
      "firstName": "Ava",
      "importResult": "string",
      "lastName": "Chen",
      "leadId": "string",
      "notes": "string",
      "phone": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/phoneBurner/latest/actions/create-contact).
