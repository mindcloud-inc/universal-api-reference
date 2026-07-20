# Explodely Universal API Examples

These examples use the MindCloud API key and Explodely connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Add Affiliate To Affiliate Referral Contract

Updates an affiliate referral contract in Explodely by adding an affiliate.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/explodely/latest/actions/add-affiliate-to-affiliate-referral-contract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contractId": "12345",
  "affiliateUsername": "affiliate_username"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/explodely/latest/actions/add-affiliate-to-affiliate-referral-contract', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contractId": "12345",
    "affiliateUsername": "affiliate_username"
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
      "added": "string",
      "error": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Affiliate To Affiliate Referral Contract action reference](actions/add-affiliate-to-affiliate-referral-contract.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/explodely/latest/actions/add-affiliate-to-affiliate-referral-contract).
