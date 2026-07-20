# Pabbly Subscription Billing: Dashboard Stats



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/dashboard-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/dashboard-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/dashboard-stats?${params}`, {
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
      "mrr": "string",
      "totalAffiliateCommissionAmount": 1,
      "totalAffiliateCount": 1,
      "totalAffiliateSalesAmount": 1,
      "totalCancelledSubscriptionAmount": 1,
      "totalCancelledSubscriptionCount": 1,
      "totalCustomerCount": 1,
      "totalNetAmountViaAffiliate": 1,
      "totalNetRevenue": 1,
      "totalOnetimeSalesAmount": 1,
      "totalOnetimeSalesCount": 1,
      "totalPaidCustomerCount": 1,
      "totalRebillAmount": 1,
      "totalRebillSubscriptionCount": 1,
      "totalRecurringSalesAmount": 1,
      "totalRecurringSalesCount": 1,
      "totalRefundAmount": 1,
      "totalRefundCount": 1,
      "totalSalesAmount": 1,
      "totalSalesCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mrr` | string |  |
| `totalAffiliateCommissionAmount` | number |  |
| `totalAffiliateCount` | number |  |
| `totalAffiliateSalesAmount` | number |  |
| `totalCancelledSubscriptionAmount` | number |  |
| `totalCancelledSubscriptionCount` | number |  |
| `totalCustomerCount` | number |  |
| `totalNetAmountViaAffiliate` | number |  |
| `totalNetRevenue` | number |  |
| `totalOnetimeSalesAmount` | number |  |
| `totalOnetimeSalesCount` | number |  |
| `totalPaidCustomerCount` | number |  |
| `totalRebillAmount` | number |  |
| `totalRebillSubscriptionCount` | number |  |
| `totalRecurringSalesAmount` | number |  |
| `totalRecurringSalesCount` | number |  |
| `totalRefundAmount` | number |  |
| `totalRefundCount` | number |  |
| `totalSalesAmount` | number |  |
| `totalSalesCount` | number |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `POST /v2/getdashboardstats` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/dashboard-stats.md) for the provider-specific parameters and requirements.

