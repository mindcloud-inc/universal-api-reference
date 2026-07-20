# TxtSync Universal API Examples

These examples use the MindCloud API key and TxtSync connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get System Report

Retrieves the system report from TxtSync.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/get-system-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/get-system-report?${params}`, {
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
      "balanceGBP": 1,
      "billingDate": "2026-05-07T12:00:00.000Z",
      "campaigns": [
        {}
      ],
      "contactRatingDistribution": [
        {}
      ],
      "isEnterpriseSupport": true,
      "isPremiumSupport": true,
      "monthlyTotals": [
        {}
      ],
      "optedIn": 1,
      "optedOut": 1,
      "supportPlanDowngradeOn": "2026-05-07T12:00:00.000Z",
      "tagDistribution": [
        {}
      ],
      "totalCampaigns": 1,
      "totalContacts": 1,
      "totalFrozenOutboundMessages": 1,
      "totalInboundCampaignMessages": 1,
      "totalInboundCampaignSegments": 1,
      "totalInboundMessages": 1,
      "totalInboundSegments": 1,
      "totalMessages": 1,
      "totalOutboundCampaignMessages": 1,
      "totalOutboundCampaignSegments": 1,
      "totalOutboundMessages": 1,
      "totalOutboundSegments": 1,
      "totalScheduledCampaigns": 1,
      "totalSegments": 1
    }
  ],
  "meta": {}
}
```

See the full [Get System Report action reference](actions/get-system-report.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/txtSync/latest/actions/get-system-report).

## Activate Campaign

Activates an existing campaign in TxtSync.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/activate-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/activate-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
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

See the full [Activate Campaign action reference](actions/activate-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/txtSync/latest/actions/activate-campaign).
