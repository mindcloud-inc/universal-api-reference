# TxtSync: Get System Report

Retrieves the system report from TxtSync.

```
GET https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/get-system-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TxtSync `connectionId` ([setup](../authentication.md)).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balanceGBP` | number |  |
| `billingDate` | date |  |
| `campaigns` | array<object> |  |
| `contactRatingDistribution` | array<object> |  |
| `isEnterpriseSupport` | boolean |  |
| `isPremiumSupport` | boolean |  |
| `monthlyTotals` | array<object> |  |
| `optedIn` | number |  |
| `optedOut` | number |  |
| `supportPlanDowngradeOn` | date |  |
| `tagDistribution` | array<object> |  |
| `totalCampaigns` | number |  |
| `totalContacts` | number |  |
| `totalFrozenOutboundMessages` | number |  |
| `totalInboundCampaignMessages` | number |  |
| `totalInboundCampaignSegments` | number |  |
| `totalInboundMessages` | number |  |
| `totalInboundSegments` | number |  |
| `totalMessages` | number |  |
| `totalOutboundCampaignMessages` | number |  |
| `totalOutboundCampaignSegments` | number |  |
| `totalOutboundMessages` | number |  |
| `totalOutboundSegments` | number |  |
| `totalScheduledCampaigns` | number |  |
| `totalSegments` | number |  |

## Native endpoint

Through the native TxtSync API, this operation is `GET /system/report` (base URL `https://api.txtsync.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-system-report.md) for the provider-specific parameters and requirements.

