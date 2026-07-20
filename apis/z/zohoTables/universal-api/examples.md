# Zoho Tables Universal API Examples

These examples use the MindCloud API key and Zoho Tables connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Portals

Retrieves all portals from Zoho Tables.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-portals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-portals?${params}`, {
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
      "createdBy": "string",
      "createdByMailId": "string",
      "createdTime": 1,
      "isHomePortal": true,
      "isShared": true,
      "lastModifiedBy": "string",
      "lastModifiedByMailId": "string",
      "lastModifiedTime": 1,
      "name": "Ava Chen",
      "planType": "string",
      "portalId": "string",
      "usersCount": 1
    }
  ],
  "meta": {}
}
```

See the full [List Portals action reference](actions/list-portals.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoTables/latest/actions/list-portals).

## Create Base

Creates a new base in Zoho Tables.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/create-base" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalId": 1,
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/create-base', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalId": 1,
    "workspaceId": "string"
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
      "baseId": "string",
      "color": "string",
      "icon": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Base action reference](actions/create-base.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoTables/latest/actions/create-base).
