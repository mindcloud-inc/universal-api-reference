# Remove.bg Universal API Examples

These examples use the MindCloud API key and Remove.bg connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves account credit balances from Remove.bg.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/removebg/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/removebg/latest/actions/get-account?${params}`, {
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
      "api": {
        "freeCalls": 1,
        "sizes": "string"
      },
      "credits": {
        "enterprise": 1,
        "payg": 1,
        "subscription": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/removebg/latest/actions/get-account).

## Remove Background

Creates a background-removed image in Remove.bg.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/removebg/latest/actions/remove-background" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/removebg/latest/actions/remove-background', {
  method: 'POST',
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
      "foregroundHeight": 1,
      "foregroundLeft": 1,
      "foregroundTop": 1,
      "foregroundWidth": 1,
      "resultB64": "string"
    }
  ],
  "meta": {}
}
```

See the full [Remove Background action reference](actions/remove-background.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/removebg/latest/actions/remove-background).
