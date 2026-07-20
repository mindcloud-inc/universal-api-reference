# Woodpecker.co Universal API Examples

These examples use the MindCloud API key and Woodpecker.co connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Woodpecker.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/get-current-user?${params}`, {
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
      "firm_id": 1,
      "firm_name": "Ava Chen",
      "user_email": "ava@example.com",
      "user_id": 1,
      "user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/woodpeckerco/latest/actions/get-current-user).

## Add Campaign Step

Adds a campaign step in Woodpecker.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/add-campaign-step" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/add-campaign-step', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": 1
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

See the full [Add Campaign Step action reference](actions/add-campaign-step.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/woodpeckerco/latest/actions/add-campaign-step).
