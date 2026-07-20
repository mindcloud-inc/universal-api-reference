# Browser Use Universal API Examples

These examples use the MindCloud API key and Browser Use connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Billing

Retrieves account billing details from Browser Use.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/get-account-billing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/get-account-billing?${params}`, {
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
      "additionalCreditsBalanceUsd": 1,
      "monthlyCreditsBalanceUsd": 1,
      "name": "Ava Chen",
      "planInfo": {},
      "projectId": "string",
      "rateLimit": 1,
      "totalCreditsBalanceUsd": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Account Billing action reference](actions/get-account-billing.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/browserUse/latest/actions/get-account-billing).

## Create Browser Session

Creates a browser session in Browser Use.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/create-browser-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/create-browser-session', {
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
      "cdpUrl": "https://example.com",
      "id": "string",
      "liveUrl": "https://example.com",
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "timeoutAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Browser Session action reference](actions/create-browser-session.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/browserUse/latest/actions/create-browser-session).
