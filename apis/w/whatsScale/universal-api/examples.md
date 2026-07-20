# WhatsScale Universal API Examples

These examples use the MindCloud API key and WhatsScale connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test Authentication

Retrieves your authentication details from WhatsScale.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/test-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/test-authentication?${params}`, {
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
      "message": "string",
      "sessions": [
        {}
      ],
      "success": true,
      "user": {
        "email": "ava@example.com",
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Test Authentication action reference](actions/test-authentication.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whatsScale/latest/actions/test-authentication).

## Add Tag to CRM Contact

Adds a tag to an existing WhatsScale CRM contact.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/add-tag-to-crm-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "tag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/add-tag-to-crm-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "tag": "string"
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
      "created_at": "string",
      "id": "string",
      "name": "Ava Chen",
      "phone": "string",
      "source": "string",
      "tags": [
        "string"
      ],
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Tag to CRM Contact action reference](actions/add-tag-to-crm-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whatsScale/latest/actions/add-tag-to-crm-contact).
