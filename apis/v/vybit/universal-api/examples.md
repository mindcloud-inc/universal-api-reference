# Vybit Universal API Examples

These examples use the MindCloud API key and Vybit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Profile



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-user-profile?${params}`, {
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
      "email": "ava@example.com",
      "key": "string",
      "name": "Ava Chen",
      "tier_id": 1
    }
  ],
  "meta": {}
}
```

See the full [Get User Profile action reference](actions/get-user-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vybit/latest/actions/get-user-profile).

## Create Reminder



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/create-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cron": "string",
  "key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vybit/latest/actions/create-reminder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cron": "string",
    "key": "string"
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
      "reminder": {},
      "result": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Reminder action reference](actions/create-reminder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vybit/latest/actions/create-reminder).
