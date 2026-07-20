# Contacts+ Universal API Examples

These examples use the MindCloud API key and Contacts+ connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves current account details from Contacts+.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contacts/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contacts/latest/actions/get-account?${params}`, {
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
      "accountId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "emails": [
        {
          "type": "ava@example.com",
          "value": "ava@example.com"
        }
      ],
      "profileData": {
        "name": {
          "familyName": "Ava Chen",
          "givenName": "Ava Chen"
        },
        "photos": [
          {
            "type": "string",
            "value": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/contacts/latest/actions/get-account).

## Create Contact

Creates a new contact in Contacts+.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/contacts/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contacts/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact": {}
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
      "contact": {
        "contactData": {
          "emails": [
            {
              "type": "ava@example.com",
              "value": "ava@example.com"
            }
          ],
          "name": {
            "familyName": "Ava Chen",
            "givenName": "Ava Chen"
          }
        },
        "contactId": "string",
        "created": "2026-05-07T12:00:00.000Z",
        "etag": "string",
        "updated": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/contacts/latest/actions/create-contact).
