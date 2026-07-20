# MailSlurp Email Plugin Universal API Examples

These examples use the MindCloud API key and MailSlurp Email Plugin connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Inboxes

Retrieves inboxes and email addresses from MailSlurp.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/list-inboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/list-inboxes?${params}`, {
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
      "": [
        {
          "createdAt": "string",
          "description": "string",
          "emailAddress": "ava@example.com",
          "expiresAt": "string",
          "favourite": true,
          "id": "string",
          "inboxType": "string",
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Inboxes action reference](actions/list-inboxes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailSlurpEmailPlugin/latest/actions/list-inboxes).

## Create Contact

Creates a new contact in MailSlurp.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/create-contact', {
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
      "company": "string",
      "createdAt": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "primaryEmailAddress": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailSlurpEmailPlugin/latest/actions/create-contact).
