# Outseta: List Transactions by Account

Retrieves account transactions from Outseta.

```
GET https://connect.mindcloud.co/v1/universal/outseta/latest/actions/list-transactions-by-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/list-transactions-by-account?connectionId=$CONNECTION_ID&limit=25&offset=0&accountUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outseta/latest/actions/list-transactions-by-account?${params}`, {
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
| `accountUid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Account": {
        "AccountStage": 1,
        "AccountStageLabel": "string",
        "BillingAddress": "string",
        "ClientIdentifier": "string",
        "Created": "string",
        "Deals": "string",
        "DomainName": "Ava Chen",
        "IsDemo": true,
        "LastLoginDateTime": "string",
        "LatestSubscription": "string",
        "MailingAddress": "string",
        "Name": "Ava Chen",
        "PaymentInformation": "string",
        "PersonAccount": "string",
        "PrimaryContact": "string",
        "Subscriptions": "string",
        "Uid": "string",
        "Updated": "string"
      },
      "Amount": 1,
      "BillingTransactionType": 1,
      "Created": "string",
      "Invoice": {
        "Amount": 1,
        "AmountOutstanding": 1,
        "BillingInvoiceStatus": 1,
        "Created": "string",
        "InvoiceDate": "string",
        "InvoiceLineItems": "string",
        "IsUserGenerated": true,
        "Number": 1,
        "Subscription": "string",
        "Uid": "string",
        "Updated": "string"
      },
      "TransactionDate": "string",
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
| `Account.AccountStageLabel` | string |  |
| `Account.BillingAddress` | string |  |
| `Account.ClientIdentifier` | string |  |
| `Account.Created` | string |  |
| `Account.Deals` | string |  |
| `Account.DomainName` | string |  |
| `Account.IsDemo` | boolean |  |
| `Account.LastLoginDateTime` | string |  |
| `Account.LatestSubscription` | string |  |
| `Account.MailingAddress` | string |  |
| `Account.Name` | string |  |
| `Account.PaymentInformation` | string |  |
| `Account.PersonAccount` | string |  |
| `Account.PrimaryContact` | string |  |
| `Account.Subscriptions` | string |  |
| `Account.Uid` | string |  |
| `Account.Updated` | string |  |
| `Amount` | number |  |
| `BillingTransactionType` | number |  |
| `Created` | string |  |
| `Invoice.Amount` | number |  |
| `Invoice.AmountOutstanding` | number |  |
| `Invoice.BillingInvoiceStatus` | number |  |
| `Invoice.Created` | string |  |
| `Invoice.InvoiceDate` | string |  |
| `Invoice.InvoiceLineItems` | string |  |
| `Invoice.IsUserGenerated` | boolean |  |
| `Invoice.Number` | number |  |
| `Invoice.Subscription` | string |  |
| `Invoice.Uid` | string |  |
| `Invoice.Updated` | string |  |
| `TransactionDate` | string |  |
| `Uid` | string |  |
| `Updated` | string |  |

## Native endpoint

Through the native Outseta API, this operation is `GET /billing/transactions/:accountUid` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transactions-by-account.md) for the provider-specific parameters and requirements.

