# WaiverForever Universal API Examples

These examples use the MindCloud API key and WaiverForever connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Info

Retrieves user info from WaiverForever.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-user-info?${params}`, {
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
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get User Info action reference](actions/get-user-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/waiverForever/latest/actions/get-user-info).

## Accept Waiver

Accepts a waiver in WaiverForever.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/accept-waiver" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "waiverId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/accept-waiver', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "waiverId": "string"
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
      "msg": "string",
      "result": true
    }
  ],
  "meta": {}
}
```

See the full [Accept Waiver action reference](actions/accept-waiver.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/waiverForever/latest/actions/accept-waiver).
