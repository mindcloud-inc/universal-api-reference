# Smsmobileapi Universal API Examples

These examples use the MindCloud API key and Smsmobileapi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Connected Mobiles

Retrieves connected gateway mobiles from Smsmobileapi.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/list-connected-mobiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/list-connected-mobiles?${params}`, {
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
      "connected_available": 1,
      "connected_limit": 1,
      "connected_now": 1,
      "filters": {},
      "items": [
        {}
      ],
      "note": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [List Connected Mobiles action reference](actions/list-connected-mobiles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smsmobileapi/latest/actions/list-connected-mobiles).

## Set WhatsApp Retrieval Status

Updates WhatsApp retrieval status in Smsmobileapi.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/set-whatsapp-retrieval-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "statut": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/set-whatsapp-retrieval-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "statut": "0"
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
      "read_message_active": 1,
      "status_note": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Set WhatsApp Retrieval Status action reference](actions/set-whatsapp-retrieval-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smsmobileapi/latest/actions/set-whatsapp-retrieval-status).
