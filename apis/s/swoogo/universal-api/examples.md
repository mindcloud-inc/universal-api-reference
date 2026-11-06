# Swoogo Universal API Examples

These examples use the MindCloud API key and Swoogo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Events



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swoogo/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swoogo/latest/actions/list-events?${params}`, {
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
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Events action reference](actions/list-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/swoogo/latest/actions/list-events).

## Update Registrant Contact ID



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/swoogo/latest/actions/update-registrant-contact-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "registrantId": 1,
  "zohoContactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swoogo/latest/actions/update-registrant-contact-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "registrantId": 1,
    "zohoContactId": "string"
  })
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

See the full [Update Registrant Contact ID action reference](actions/update-registrant-contact-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/swoogo/latest/actions/update-registrant-contact-id).
