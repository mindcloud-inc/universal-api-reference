# Scrapeless Universal API Examples

These examples use the MindCloud API key and Scrapeless connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Info

Retrieves user information from Scrapeless.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-user-info?${params}`, {
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
      "credits": "string",
      "excessCredits": "string",
      "plan": {
        "credits": "string",
        "endAt": "string",
        "price": 1,
        "status": 1,
        "usage": 1
      },
      "status": 1,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User Info action reference](actions/get-user-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scrapeless/latest/actions/get-user-info).

## Configure 1Password Integration

Updates the 1Password integration in Scrapeless.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/configure-1password-integration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "token": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/configure-1password-integration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "token": "string"
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

See the full [Configure 1Password Integration action reference](actions/configure-1password-integration.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scrapeless/latest/actions/configure-1password-integration).
