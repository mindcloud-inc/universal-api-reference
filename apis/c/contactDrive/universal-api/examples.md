# ContactDrive Universal API Examples

These examples use the MindCloud API key and ContactDrive connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactDrive/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactDrive/latest/actions/list-contacts?${params}`, {
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
      "city": "string",
      "company": "string",
      "contactedAt": "2026-05-07T12:00:00.000Z",
      "country": "string",
      "county": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "emailAddress": "ava@example.com",
      "firstName": "Ava",
      "fullname": "Ava Chen",
      "gender": "string",
      "id": "string",
      "jobTitle": "string",
      "lastName": "Chen",
      "middleName": "Ava Chen",
      "nickname": "Ava Chen",
      "phone": "string",
      "prefix": "string",
      "state": "string",
      "street": "string",
      "suffix": "string",
      "tags": [
        [
          "string"
        ]
      ],
      "transactionTotal": 1,
      "zip": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/contactDrive/latest/actions/list-contacts).

## Create Or Update Contact



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/contactDrive/latest/actions/create-or-update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contactDrive/latest/actions/create-or-update-contact', {
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
      "city": "string",
      "company": "string",
      "contactedAt": "2026-05-07T12:00:00.000Z",
      "country": "string",
      "county": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "emailAddress": "ava@example.com",
      "firstName": "Ava",
      "fullname": "Ava Chen",
      "gender": "string",
      "id": "string",
      "jobTitle": "string",
      "lastName": "Chen",
      "middleName": "Ava Chen",
      "nickname": "Ava Chen",
      "phone": "string",
      "prefix": "string",
      "state": "string",
      "street": "string",
      "suffix": "string",
      "tags": [
        [
          "string"
        ]
      ],
      "transactionTotal": 1,
      "zip": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Or Update Contact action reference](actions/create-or-update-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/contactDrive/latest/actions/create-or-update-contact).
