# DitLead Universal API Examples

These examples use the MindCloud API key and DitLead connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate API Key



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/validate-api-key?connectionId=$CONNECTION_ID&keyType=platform" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyType": "platform"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/validate-api-key?${params}`, {
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
      "data": {
        "apiKeyData": {
          "_id": "string",
          "name": "Ava Chen"
        },
        "keyType": "string",
        "projectData": {
          "id": "string",
          "name": "Ava Chen",
          "slug": "string"
        }
      },
      "isValid": true,
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Validate API Key action reference](actions/validate-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ditLead/latest/actions/validate-api-key).

## Add Contact To List



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/add-contact-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "listId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/add-contact-to-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "listId": "string"
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
      "data": {
        "message": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Contact To List action reference](actions/add-contact-to-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ditLead/latest/actions/add-contact-to-list).
