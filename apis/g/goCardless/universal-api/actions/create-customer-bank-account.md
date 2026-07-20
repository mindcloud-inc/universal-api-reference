# GoCardless: Create Customer Bank Account

Creates a new customer bank account in GoCardless.

```
POST https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/create-customer-bank-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/create-customer-bank-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "links.customer": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/create-customer-bank-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "links.customer": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountHolderName` | string | no |  |
| `accountNumber` | string | no |  |
| `bankCode` | string | no |  |
| `branchCode` | string | no |  |
| `countryCode` | string | no |  |
| `currency` | list | no | One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `iban` | string | no |  |
| `links` | object | no |  |
| `links.customer` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountType` | string | no |  |
| `metadata` | object | no |  |
| `links.customerBankAccountToken` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerBankAccounts": {
        "accountHolderName": "Ava Chen",
        "accountNumberEnding": "string",
        "accountType": {},
        "bankName": "Ava Chen",
        "countryCode": "string",
        "createdAt": "string",
        "currency": "string",
        "enabled": true,
        "id": "string",
        "links": {
          "customer": "https://example.com"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerBankAccounts.accountHolderName` | string |  |
| `customerBankAccounts.accountNumberEnding` | string |  |
| `customerBankAccounts.accountType` | object |  |
| `customerBankAccounts.bankName` | string |  |
| `customerBankAccounts.countryCode` | string |  |
| `customerBankAccounts.createdAt` | string |  |
| `customerBankAccounts.currency` | string |  |
| `customerBankAccounts.enabled` | boolean |  |
| `customerBankAccounts.id` | string |  |
| `customerBankAccounts.links.customer` | string |  |

## Native endpoint

Through the native GoCardless API, this operation is `POST /customer_bank_accounts` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-bank-account.md) for the provider-specific parameters and requirements.

