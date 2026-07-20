# WhatsBox Universal API Examples

These examples use the MindCloud API key and WhatsBox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Organization

Retrieves your organization details from WhatsBox.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/get-my-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/get-my-organization?${params}`, {
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
      "businessName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get My Organization action reference](actions/get-my-organization.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whatsBox/latest/actions/get-my-organization).

## Create Contact List

Creates a new contact list in WhatsBox.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/create-contact-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/create-contact-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Contact List action reference](actions/create-contact-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whatsBox/latest/actions/create-contact-list).
