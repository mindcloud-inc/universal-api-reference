# Zoominfo Universal API Examples

These examples use the MindCloud API key and Zoominfo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Usage

Retrieves usage details from ZoomInfo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/get-usage?${params}`, {
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
      "usage": [
        {
          "currentUsage": 1,
          "description": "string",
          "limitType": "string",
          "totalLimit": 1,
          "usageRemaining": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Usage action reference](actions/get-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zoominfo/latest/actions/get-usage).

## Authenticate

Creates an authentication token in ZoomInfo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/authenticate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "{{credentials.userName}}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/authenticate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "{{credentials.userName}}"
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
      "jwt": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Authenticate action reference](actions/authenticate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zoominfo/latest/actions/authenticate).
