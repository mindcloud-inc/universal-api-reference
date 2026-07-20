# Pinghome Universal API Examples

These examples use the MindCloud API key and Pinghome connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Customer Profile

Retrieves customer profile information from Pinghome.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/get-customer-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/get-customer-profile?${params}`, {
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

See the full [Get Customer Profile action reference](actions/get-customer-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pinghome/latest/actions/get-customer-profile).

## Change Uptime Monitor Status

Updates uptime monitor status in Pinghome.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/change-uptime-monitor-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "enabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/change-uptime-monitor-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "enabled": true
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

See the full [Change Uptime Monitor Status action reference](actions/change-uptime-monitor-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pinghome/latest/actions/change-uptime-monitor-status).
