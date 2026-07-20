# RevenueCat Universal API Examples

These examples use the MindCloud API key and RevenueCat connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves projects from RevenueCat.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/list-projects?${params}`, {
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
      "archived_at": "string",
      "cancelled_at": "string",
      "code": "string",
      "created_at": "string",
      "deleted_at": "string",
      "display_name": "Ava Chen",
      "expires_at": "string",
      "id": "string",
      "items": [
        {}
      ],
      "metrics": [
        {}
      ],
      "name": "Ava Chen",
      "next_page": "string",
      "object": "string",
      "refunded_at": "string",
      "status": "string",
      "store_identifier": "string",
      "success": true,
      "updated_at": "string",
      "url": "https://example.com",
      "value": 1
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/revenueCat/latest/actions/list-projects).

## Archive Entitlement

Archives an entitlement in RevenueCat.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/archive-entitlement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/archive-entitlement', {
  method: 'PUT',
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
      "deleted_at": "string",
      "id": "string",
      "items": [
        {}
      ],
      "object": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Archive Entitlement action reference](actions/archive-entitlement.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/revenueCat/latest/actions/archive-entitlement).
