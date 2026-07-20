# Chatling Universal API Examples

These examples use the MindCloud API key and Chatling connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Settings

Retrieves project settings from Chatling.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatling/latest/actions/list-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatling/latest/actions/list-settings?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Settings action reference](actions/list-settings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatling/latest/actions/list-settings).

## Create Contact

Creates a new contact in Chatling.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatling/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatbotId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatling/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatbotId": "string"
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatling/latest/actions/create-contact).
