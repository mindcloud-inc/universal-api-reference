# 2Smart Cloud Universal API Examples

These examples use the MindCloud API key and 2Smart Cloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get vendor info



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-profile?${params}`, {
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
      "avatar_url": "https://example.com",
      "category": "string",
      "created": "string",
      "id": 1,
      "is_blocked": true,
      "login": "string",
      "mqttCredentials": {},
      "updated": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get vendor info action reference](actions/get-vendor-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartCloud/latest/actions/get-vendor-profile).

## Bulk update favorite widgets groups positions



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/bulk-update-favorite-widget-groups-bulk-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/bulk-update-favorite-widget-groups-bulk-update', {
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
      "data": [
        {}
      ],
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Bulk update favorite widgets groups positions action reference](actions/bulk-update-favorite-widget-groups-bulk-update.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartCloud/latest/actions/bulk-update-favorite-widget-groups-bulk-update).
