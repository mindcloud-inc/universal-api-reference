# Vercel Universal API Examples

These examples use the MindCloud API key and Vercel connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User

Retrieves the authenticated user from Vercel.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-user?${params}`, {
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
      "avatar": {},
      "billing": {
        "address": {},
        "cancelation": {},
        "currency": "string",
        "email": {},
        "language": {},
        "name": {},
        "period": {},
        "plan": "string",
        "platform": "string",
        "status": "string",
        "tax": {},
        "trial": {}
      },
      "createdAt": 1,
      "dataCache": {
        "excessBillingEnabled": true
      },
      "defaultTeamId": "string",
      "email": "ava@example.com",
      "hasTrialAvailable": true,
      "id": "string",
      "name": {},
      "remoteCaching": {
        "enabled": true
      },
      "resourceConfig": {
        "concurrentBuilds": 1
      },
      "softBlock": {},
      "stagingPrefix": "string",
      "username": "Ava Chen",
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User action reference](actions/get-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vercel/latest/actions/get-user).

## Add Domain

Adds an existing domain to Vercel.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/add-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vercel/latest/actions/add-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "domain": {}
    }
  ],
  "meta": {}
}
```

See the full [Add Domain action reference](actions/add-domain.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vercel/latest/actions/add-domain).
