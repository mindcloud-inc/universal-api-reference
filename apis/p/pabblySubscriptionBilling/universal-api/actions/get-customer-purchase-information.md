# Pabbly Subscription Billing: Get Customer Purchase Information



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-customer-purchase-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-customer-purchase-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-customer-purchase-information?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currencyCode` | string | no | Eg: USD, INR |
| `customerId` | string | no | Pabbly Customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "puchaseInfo": {
        "appliedTax": [
          "string"
        ],
        "appliedTaxTotal": {
          "saleCount": 1,
          "taxAmount": 1,
          "taxCount": 1
        },
        "mrrtotalamt": 1,
        "receivablesAmount": 1,
        "refundAmount": 1,
        "totalAmount": 1,
        "totalRevenue": 1,
        "unusedCredit": {
          "remainingAmount": 1,
          "subscriptionCount": 1
        }
      },
      "subscriptionInfo": {
        "cancelledAmount": 1,
        "cancelledCount": 1,
        "expiredAmount": 1,
        "expiredCount": 1,
        "failedAmount": 1,
        "failedCount": 1,
        "liveAmount": 1,
        "liveCount": 1,
        "nonrenewingAmount": 1,
        "nonrenewingCount": 1,
        "onetimeAddonAmount": 1,
        "onetimeAddonCount": 1,
        "onetimeAmount": 1,
        "onetimeCount": 1,
        "pendingAmount": 1,
        "pendingCount": 1,
        "reccuringAmount": 1,
        "reccuringCount": 1,
        "recurringAddonAmount": 1,
        "recurringAddonCount": 1,
        "totalAddonAmount": 1,
        "totalAddonCount": 1,
        "totalAmount": 1,
        "totalCount": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `puchaseInfo.appliedTax[]` | string |  |
| `puchaseInfo.appliedTaxTotal.saleCount` | number |  |
| `puchaseInfo.appliedTaxTotal.taxAmount` | number |  |
| `puchaseInfo.appliedTaxTotal.taxCount` | number |  |
| `puchaseInfo.mrrtotalamt` | number |  |
| `puchaseInfo.receivablesAmount` | number |  |
| `puchaseInfo.refundAmount` | number |  |
| `puchaseInfo.totalAmount` | number |  |
| `puchaseInfo.totalRevenue` | number |  |
| `puchaseInfo.unusedCredit.remainingAmount` | number |  |
| `puchaseInfo.unusedCredit.subscriptionCount` | number |  |
| `subscriptionInfo.cancelledAmount` | number |  |
| `subscriptionInfo.cancelledCount` | number |  |
| `subscriptionInfo.expiredAmount` | number |  |
| `subscriptionInfo.expiredCount` | number |  |
| `subscriptionInfo.failedAmount` | number |  |
| `subscriptionInfo.failedCount` | number |  |
| `subscriptionInfo.liveAmount` | number |  |
| `subscriptionInfo.liveCount` | number |  |
| `subscriptionInfo.nonrenewingAmount` | number |  |
| `subscriptionInfo.nonrenewingCount` | number |  |
| `subscriptionInfo.onetimeAddonAmount` | number |  |
| `subscriptionInfo.onetimeAddonCount` | number |  |
| `subscriptionInfo.onetimeAmount` | number |  |
| `subscriptionInfo.onetimeCount` | number |  |
| `subscriptionInfo.pendingAmount` | number |  |
| `subscriptionInfo.pendingCount` | number |  |
| `subscriptionInfo.reccuringAmount` | number |  |
| `subscriptionInfo.reccuringCount` | number |  |
| `subscriptionInfo.recurringAddonAmount` | number |  |
| `subscriptionInfo.recurringAddonCount` | number |  |
| `subscriptionInfo.totalAddonAmount` | number |  |
| `subscriptionInfo.totalAddonCount` | number |  |
| `subscriptionInfo.totalAmount` | number |  |
| `subscriptionInfo.totalCount` | number |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `GET /v1/customer/purchase-info/:customerId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-purchase-information.md) for the provider-specific parameters and requirements.

