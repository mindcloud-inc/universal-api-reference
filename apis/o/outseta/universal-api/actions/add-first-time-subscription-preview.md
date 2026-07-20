# Outseta: Add First Time Subscription Preview

Retrieves a first-time subscription charge preview from Outseta.

```
POST https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-first-time-subscription-preview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-first-time-subscription-preview" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-first-time-subscription-preview', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `asOf` | string | no |  |
| `plan.uid` | string | no |  |
| `billingRenewalTerm` | number | no |  |
| `account` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Amount": 1,
      "AmountOutstanding": 1,
      "BillingInvoiceStatus": 1,
      "Created": "string",
      "InvoiceDate": "string",
      "InvoiceLineItems": [
        {
          "Amount": 1,
          "Created": "string",
          "Description": "string",
          "EndDate": "string",
          "Invoice": "string",
          "Quantity": "string",
          "Rate": 1,
          "StartDate": "string",
          "Tax": 1,
          "Uid": "string",
          "UnitOfMeasure": "string",
          "Updated": "string"
        }
      ],
      "IsUserGenerated": true,
      "Number": 1,
      "Subscription": {
        "Account": "string",
        "BillingRenewalTerm": 1,
        "Created": "string",
        "EndDate": "string",
        "IsPlanUpgradeRequired": true,
        "NewRequiredQuantity": "string",
        "Plan": "string",
        "PlanUpgradeRequiredMessage": "string",
        "Quantity": "string",
        "RenewalDate": "string",
        "StartDate": "string",
        "SubscriptionAddOns": "string",
        "Uid": "string",
        "Updated": "string"
      },
      "Uid": "string",
      "Updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Amount` | number |  |
| `AmountOutstanding` | number |  |
| `BillingInvoiceStatus` | number |  |
| `Created` | string |  |
| `InvoiceDate` | string |  |
| `InvoiceLineItems` | array<object> |  |
| `InvoiceLineItems[].Amount` | number |  |
| `InvoiceLineItems[].Created` | string |  |
| `InvoiceLineItems[].Description` | string |  |
| `InvoiceLineItems[].EndDate` | string |  |
| `InvoiceLineItems[].Invoice` | string |  |
| `InvoiceLineItems[].Quantity` | string |  |
| `InvoiceLineItems[].Rate` | number |  |
| `InvoiceLineItems[].StartDate` | string |  |
| `InvoiceLineItems[].Tax` | number |  |
| `InvoiceLineItems[].Uid` | string |  |
| `InvoiceLineItems[].UnitOfMeasure` | string |  |
| `InvoiceLineItems[].Updated` | string |  |
| `IsUserGenerated` | boolean |  |
| `Number` | number |  |
| `Subscription.Account` | string |  |
| `Subscription.BillingRenewalTerm` | number |  |
| `Subscription.Created` | string |  |
| `Subscription.EndDate` | string |  |
| `Subscription.IsPlanUpgradeRequired` | boolean |  |
| `Subscription.NewRequiredQuantity` | string |  |
| `Subscription.Plan` | string |  |
| `Subscription.PlanUpgradeRequiredMessage` | string |  |
| `Subscription.Quantity` | string |  |
| `Subscription.RenewalDate` | string |  |
| `Subscription.StartDate` | string |  |
| `Subscription.SubscriptionAddOns` | string |  |
| `Subscription.Uid` | string |  |
| `Subscription.Updated` | string |  |
| `Uid` | string |  |
| `Updated` | string |  |

## Native endpoint

Through the native Outseta API, this operation is `POST /billing/subscriptions/compute-charge-summary` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-first-time-subscription-preview.md) for the provider-specific parameters and requirements.

