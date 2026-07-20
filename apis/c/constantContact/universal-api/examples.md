# Constant Contact Universal API Examples

These examples use the MindCloud API key and Constant Contact connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Contact Consent Counts

Retrieves contact consent counts from Constant Contact.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/get-contact-consent-counts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/get-contact-consent-counts?${params}`, {
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
      "explicit": 1,
      "implicit": 1,
      "pending": 1,
      "total": 1,
      "unsubscribed": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Contact Consent Counts action reference](actions/get-contact-consent-counts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/constantContact/latest/actions/get-contact-consent-counts).

## Create Contact

Creates a contact in Constant Contact.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "person@example.com",
  "permissionToSend": "Select permission level",
  "createSource": "Account"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "person@example.com",
    "permissionToSend": "Select permission level",
    "createSource": "Account"
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
      "contactId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createSource": "string",
      "emailAddress": {},
      "firstName": "Ava",
      "lastName": "Chen",
      "listMemberships": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/constantContact/latest/actions/create-contact).
