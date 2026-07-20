# Proofly Universal API Examples

These examples use the MindCloud API key and Proofly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User

Retrieves account details from your Proofly account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proofly/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proofly/latest/actions/get-user?${params}`, {
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
      "impressions": {},
      "meta": {},
      "name": "Ava Chen",
      "pixel": {}
    }
  ],
  "meta": {}
}
```

See the full [Get User action reference](actions/get-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/proofly/latest/actions/get-user).

## Toggle Campaign

Toggles a campaign between active and inactive in Proofly.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/proofly/latest/actions/toggle-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proofly/latest/actions/toggle-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string"
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Toggle Campaign action reference](actions/toggle-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/proofly/latest/actions/toggle-campaign).
