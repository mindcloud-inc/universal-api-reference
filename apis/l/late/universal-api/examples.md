# Late Universal API Examples

These examples use the MindCloud API key and Late connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Usage Stats



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/late/latest/actions/get-usage-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/late/latest/actions/get-usage-stats?${params}`, {
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
      "autoUpgradeEnabled": true,
      "billingAnchorDay": 1,
      "billingPeriod": "string",
      "hasAccess": true,
      "isAppSumo": true,
      "isInvitedUser": true,
      "isRestrictedUser": true,
      "limits": {},
      "planName": "Ava Chen",
      "signupDate": "2026-05-07T12:00:00.000Z",
      "suspendedAt": "2026-05-07T12:00:00.000Z",
      "usage": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Usage Stats action reference](actions/get-usage-stats.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/late/latest/actions/get-usage-stats).

## Create Post



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/late/latest/actions/create-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/late/latest/actions/create-post', {
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
      "message": "string",
      "post": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Post action reference](actions/create-post.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/late/latest/actions/create-post).
