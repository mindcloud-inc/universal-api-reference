# Wati Universal API Examples

These examples use the MindCloud API key and Wati connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Message Templates

Retrieves available message templates from Wati.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wati/latest/actions/list-message-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wati/latest/actions/list-message-templates?${params}`, {
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
      "addSecurityRecommendation": true,
      "body": "string",
      "bodyOriginal": "string",
      "buttons": [
        {}
      ],
      "buttonsType": "string",
      "category": "string",
      "customParams": [
        {}
      ],
      "elementName": "Ava Chen",
      "expiresIn": 1,
      "footer": "string",
      "header": {},
      "hsm": "string",
      "hsmOriginal": "string",
      "id": "string",
      "includeExpiryTime": true,
      "language": {},
      "lastModified": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Message Templates action reference](actions/list-message-templates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wati/latest/actions/list-message-templates).

## Add Contact

Creates a new contact in Wati.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wati/latest/actions/add-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "whatsappNumber": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wati/latest/actions/add-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "whatsappNumber": "string",
    "name": "Ava Chen"
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
      "info": "string",
      "result": true
    }
  ],
  "meta": {}
}
```

See the full [Add Contact action reference](actions/add-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wati/latest/actions/add-contact).
