# Outseta: Get Subscription

Retrieves a subscription from Outseta.

```
GET https://connect.mindcloud.co/v1/universal/outseta/latest/actions/get-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/get-subscription?connectionId=$CONNECTION_ID&subscriptionUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriptionUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outseta/latest/actions/get-subscription?${params}`, {
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
| `subscriptionUid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Account": {
        "AccountStage": 1,
        "BillingAddress": "string",
        "ClientIdentifier": "string",
        "Created": "string",
        "MailingAddress": "string",
        "Name": "Ava Chen",
        "PaymentInformation": "string",
        "PersonAccount": "string",
        "Subscriptions": "string",
        "Uid": "string",
        "Updated": "string"
      },
      "BillingRenewalTerm": 1,
      "Created": "string",
      "EndDate": "string",
      "IsPlanUpgradeRequired": true,
      "NewRequiredQuantity": "string",
      "Plan": {
        "AnnualRate": 1,
        "Created": "string",
        "IsQuantityEditable": true,
        "IsTaxable": true,
        "MinimumQuantity": 1,
        "MonthlyRate": 1,
        "Name": "Ava Chen",
        "PlanAddOns": "string",
        "PlanFamily": "string",
        "SetupFee": 1,
        "TrialPeriodDays": 1,
        "Uid": "string",
        "UnitOfMeasure": "string",
        "Updated": "string"
      },
      "PlanUpgradeRequiredMessage": "string",
      "Quantity": "string",
      "RenewalDate": "string",
      "StartDate": "string",
      "SubscriptionAddOns": [
        {
          "AddOn": "string",
          "BillingRenewalTerm": 1,
          "Created": "string",
          "EndDate": "string",
          "NewRequiredQuantity": "string",
          "Quantity": "string",
          "RenewalDate": "string",
          "StartDate": "string",
          "Subscription": "string",
          "Uid": "string",
          "Updated": "string"
        }
      ],
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
| `Account.AccountStage` | number |  |
| `Account.BillingAddress` | string |  |
| `Account.ClientIdentifier` | string |  |
| `Account.Created` | string |  |
| `Account.MailingAddress` | string |  |
| `Account.Name` | string |  |
| `Account.PaymentInformation` | string |  |
| `Account.PersonAccount` | string |  |
| `Account.Subscriptions` | string |  |
| `Account.Uid` | string |  |
| `Account.Updated` | string |  |
| `BillingRenewalTerm` | number |  |
| `Created` | string |  |
| `EndDate` | string |  |
| `IsPlanUpgradeRequired` | boolean |  |
| `NewRequiredQuantity` | string |  |
| `Plan.AnnualRate` | number |  |
| `Plan.Created` | string |  |
| `Plan.IsQuantityEditable` | boolean |  |
| `Plan.IsTaxable` | boolean |  |
| `Plan.MinimumQuantity` | number |  |
| `Plan.MonthlyRate` | number |  |
| `Plan.Name` | string |  |
| `Plan.PlanAddOns` | string |  |
| `Plan.PlanFamily` | string |  |
| `Plan.SetupFee` | number |  |
| `Plan.TrialPeriodDays` | number |  |
| `Plan.Uid` | string |  |
| `Plan.UnitOfMeasure` | string |  |
| `Plan.Updated` | string |  |
| `PlanUpgradeRequiredMessage` | string |  |
| `Quantity` | string |  |
| `RenewalDate` | string |  |
| `StartDate` | string |  |
| `SubscriptionAddOns` | array<object> |  |
| `SubscriptionAddOns[].AddOn` | string |  |
| `SubscriptionAddOns[].BillingRenewalTerm` | number |  |
| `SubscriptionAddOns[].Created` | string |  |
| `SubscriptionAddOns[].EndDate` | string |  |
| `SubscriptionAddOns[].NewRequiredQuantity` | string |  |
| `SubscriptionAddOns[].Quantity` | string |  |
| `SubscriptionAddOns[].RenewalDate` | string |  |
| `SubscriptionAddOns[].StartDate` | string |  |
| `SubscriptionAddOns[].Subscription` | string |  |
| `SubscriptionAddOns[].Uid` | string |  |
| `SubscriptionAddOns[].Updated` | string |  |
| `Uid` | string |  |
| `Updated` | string |  |

## Native endpoint

Through the native Outseta API, this operation is `GET /billing/subscriptions/:subscriptionUid` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription.md) for the provider-specific parameters and requirements.

