# BrowserStack Universal API Examples

These examples use the MindCloud API key and BrowserStack connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Automate Plan Details

Retrieves Automate plan details from BrowserStack.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserStack/latest/actions/get-automate-plan-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserStack/latest/actions/get-automate-plan-details?${params}`, {
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

See the full [Get Automate Plan Details action reference](actions/get-automate-plan-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/browserStack/latest/actions/get-automate-plan-details).

## Set Session Status

Updates a session status in BrowserStack Automate.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/browserStack/latest/actions/set-session-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "string",
  "status": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/browserStack/latest/actions/set-session-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "string",
    "status": "0"
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

See the full [Set Session Status action reference](actions/set-session-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/browserStack/latest/actions/set-session-status).
