# Bridge: Get Account

Retrieves an account from Bridge.

```
GET https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-account?connectionId=$CONNECTION_ID&userAccessToken=string&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userAccessToken": "string",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-account?${params}`, {
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
| `userAccessToken` | string | yes | Bridge user access token returned by the Authorization token action. |
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountingBalance": 1,
      "balance": 1,
      "currencyCode": "string",
      "dataAccess": "string",
      "iban": "string",
      "id": 1,
      "instantBalance": 1,
      "itemId": 1,
      "lastRefreshStatus": "string",
      "loanDetails": {
        "borrowedCapital": 1,
        "interestRate": 1,
        "maturityDate": "2026-05-07T12:00:00.000Z",
        "nextPaymentAmount": 1,
        "nextPaymentDate": "2026-05-07T12:00:00.000Z",
        "openingDate": "2026-05-07T12:00:00.000Z",
        "remainingCapital": 1,
        "repaidCapital": 1,
        "type": "string"
      },
      "name": "Ava Chen",
      "pro": true,
      "providerId": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountingBalance` | number | Accounting balance represents the available money excluding pending and processing transactions |
| `balance` | number | Account's balance |
| `currencyCode` | string | 3 letters ISO 4217 currency code |
| `dataAccess` | string | User approved access to this account |
| `iban` | string | The IBAN of the bank account |
| `id` | number | Account's unique identifier |
| `instantBalance` | number | Instant balance represents the expected money on the account including pending and processing transactions |
| `itemId` | number | Identifier of the account's item |
| `lastRefreshStatus` | string | Indicate if the account was updated successfully or not during the last refresh of the item |
| `loanDetails` | object |  |
| `loanDetails.borrowedCapital` | number | Amount of capital that was borrowed |
| `loanDetails.interestRate` | number | Loan's interest rate |
| `loanDetails.maturityDate` | date | Predicted end of the loan's refunding |
| `loanDetails.nextPaymentAmount` | number | Amount owed for the next payment |
| `loanDetails.nextPaymentDate` | date | Date when the next payment is owed |
| `loanDetails.openingDate` | date | Date when the loan was contracted |
| `loanDetails.remainingCapital` | number | Amount of capital left to repay |
| `loanDetails.repaidCapital` | number | Amount of capital that has already been repaid. |
| `loanDetails.type` | string | Loan type |
| `name` | string | Account's name taken from the provider's website |
| `pro` | boolean | Flag to indicate that the account is a business account |
| `providerId` | number | Identifier of the account's provider |
| `type` | string | Account's type |
| `updatedAt` | date | Timestamp recording when the account was last updated |

## Native endpoint

Through the native Bridge API, this operation is `GET /aggregation/accounts/:id` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

