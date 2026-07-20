# Outseta: List Accounts

Retrieves a list of accounts from Outseta.

```
GET https://connect.mindcloud.co/v1/universal/outseta/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outseta/latest/actions/list-accounts?${params}`, {
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
      "AccountStage": 1,
      "BillingAddress": {
        "AddressLine1": "string",
        "AddressLine2": "string",
        "AddressLine3": "string",
        "City": "string",
        "Created": "string",
        "PostalCode": "string",
        "State": "string",
        "Uid": "string",
        "Updated": "string"
      },
      "ClientIdentifier": "string",
      "Created": "string",
      "MailingAddress": {
        "AddressLine1": "string",
        "AddressLine2": "string",
        "AddressLine3": "string",
        "City": "string",
        "Created": "string",
        "PostalCode": "string",
        "State": "string",
        "Uid": "string",
        "Updated": "string"
      },
      "Name": "Ava Chen",
      "PaymentInformation": "string",
      "PersonAccount": [
        {
          "Account": "string",
          "Created": "string",
          "IsPrimary": true,
          "Person": "string",
          "Uid": "string",
          "Updated": "string"
        }
      ],
      "Subscriptions": [
        {
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
| `AccountStage` | number |  |
| `BillingAddress.AddressLine1` | string |  |
| `BillingAddress.AddressLine2` | string |  |
| `BillingAddress.AddressLine3` | string |  |
| `BillingAddress.City` | string |  |
| `BillingAddress.Created` | string |  |
| `BillingAddress.PostalCode` | string |  |
| `BillingAddress.State` | string |  |
| `BillingAddress.Uid` | string |  |
| `BillingAddress.Updated` | string |  |
| `ClientIdentifier` | string |  |
| `Created` | string |  |
| `MailingAddress.AddressLine1` | string |  |
| `MailingAddress.AddressLine2` | string |  |
| `MailingAddress.AddressLine3` | string |  |
| `MailingAddress.City` | string |  |
| `MailingAddress.Created` | string |  |
| `MailingAddress.PostalCode` | string |  |
| `MailingAddress.State` | string |  |
| `MailingAddress.Uid` | string |  |
| `MailingAddress.Updated` | string |  |
| `Name` | string |  |
| `PaymentInformation` | string |  |
| `PersonAccount` | array<object> |  |
| `PersonAccount[].Account` | string |  |
| `PersonAccount[].Created` | string |  |
| `PersonAccount[].IsPrimary` | boolean |  |
| `PersonAccount[].Person` | string |  |
| `PersonAccount[].Uid` | string |  |
| `PersonAccount[].Updated` | string |  |
| `Subscriptions` | array<object> |  |
| `Subscriptions[].Account` | string |  |
| `Subscriptions[].BillingRenewalTerm` | number |  |
| `Subscriptions[].Created` | string |  |
| `Subscriptions[].EndDate` | string |  |
| `Subscriptions[].IsPlanUpgradeRequired` | boolean |  |
| `Subscriptions[].NewRequiredQuantity` | string |  |
| `Subscriptions[].Plan` | string |  |
| `Subscriptions[].PlanUpgradeRequiredMessage` | string |  |
| `Subscriptions[].Quantity` | string |  |
| `Subscriptions[].RenewalDate` | string |  |
| `Subscriptions[].StartDate` | string |  |
| `Subscriptions[].SubscriptionAddOns` | string |  |
| `Subscriptions[].Uid` | string |  |
| `Subscriptions[].Updated` | string |  |
| `Uid` | string |  |
| `Updated` | string |  |

## Native endpoint

Through the native Outseta API, this operation is `GET /crm/accounts` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

