# InviteReferrals Universal API Examples

These examples use the MindCloud API key and InviteReferrals connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Add Conversion



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/inviteReferrals/latest/actions/add-conversion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "string",
  "campaignId": 1,
  "refereeName": "Ava Chen",
  "refereeEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inviteReferrals/latest/actions/add-conversion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "string",
    "campaignId": 1,
    "refereeName": "Ava Chen",
    "refereeEmail": "ava@example.com"
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
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Conversion action reference](actions/add-conversion.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/inviteReferrals/latest/actions/add-conversion).
