# Zoho Backstage Universal API Examples

These examples use the MindCloud API key and Zoho Backstage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Portals



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-portals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-portals?${params}`, {
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
      "domain": "string",
      "id": "string",
      "isDefault": true,
      "name": "Ava Chen",
      "ownerEmail": "ava@example.com",
      "ownerName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Portals action reference](actions/list-portals.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoBackstage/latest/actions/list-portals).

## Create Agenda



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/create-agenda" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalId": "string",
  "eventId": "string",
  "index": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/create-agenda', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalId": "string",
    "eventId": "string",
    "index": 1
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
      "agenda_id": "string",
      "created_time": "2026-05-07T12:00:00.000Z",
      "index": 1,
      "last_modified_time": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Agenda action reference](actions/create-agenda.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoBackstage/latest/actions/create-agenda).
