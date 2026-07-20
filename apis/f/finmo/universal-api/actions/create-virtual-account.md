# Finmo: Create Virtual Account

Creates a new virtual account in Finmo.

```
POST https://connect.mindcloud.co/v1/universal/finmo/latest/actions/create-virtual-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/create-virtual-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "currency": "string",
  "customerId": "string",
  "payinMethodName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/finmo/latest/actions/create-virtual-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "currency": "string",
    "customerId": "string",
    "payinMethodName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currency` | string | yes | Virtual account currency. |
| `customerId` | string | yes | Customer reference for the virtual account. |
| `scope` | string | no | Virtual account scope. |
| `creditWalletId` | string | no | Wallet ID to credit. Use instead of credit wallet category when known. |
| `creditWalletCategory` | string | no | Wallet category to credit when a wallet ID is not provided. |
| `feesWalletId` | string | no | Fees wallet ID. |
| `description` | string | no | Description for the virtual account. |
| `payinMethodName` | string | yes | Payin method name for the virtual account. |
| `payinMethodParam` | object | no | Additional payin method parameters. |
| `organizationReferenceId` | string | no | Organization reference identifier for the virtual account. |
| `webhookUrl` | string | no | Override webhook URL for this virtual account. |
| `metadata` | object | no | Custom metadata object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "createdAt": "string",
      "creditWalletId": "string",
      "currency": "string",
      "customerId": "string",
      "deletedAt": "string",
      "description": "string",
      "expireAt": "string",
      "expiredAt": "string",
      "feesCurrency": "string",
      "feesIncludingTax": 1,
      "feesWithoutTax": 1,
      "isActive": true,
      "isCancellable": true,
      "isChargeable": true,
      "isDeleted": true,
      "isExpired": true,
      "isFeesCharged": true,
      "isRefundable": true,
      "isSenderValidationEnabled": true,
      "metadata": {},
      "organizationReferenceId": "string",
      "orgId": "string",
      "payCode": {},
      "payinMethodName": "Ava Chen",
      "payinMethodParam": {},
      "scope": "string",
      "taxOnFees": 1,
      "transactionId": "string",
      "updatedAt": "string",
      "virtualAccountId": "string",
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `createdAt` | string |  |
| `creditWalletId` | string |  |
| `currency` | string |  |
| `customerId` | string |  |
| `deletedAt` | string |  |
| `description` | string |  |
| `expireAt` | string |  |
| `expiredAt` | string |  |
| `feesCurrency` | string |  |
| `feesIncludingTax` | number |  |
| `feesWithoutTax` | number |  |
| `isActive` | boolean |  |
| `isCancellable` | boolean |  |
| `isChargeable` | boolean |  |
| `isDeleted` | boolean |  |
| `isExpired` | boolean |  |
| `isFeesCharged` | boolean |  |
| `isRefundable` | boolean |  |
| `isSenderValidationEnabled` | boolean |  |
| `metadata` | object |  |
| `organizationReferenceId` | string |  |
| `orgId` | string |  |
| `payCode` | object |  |
| `payinMethodName` | string |  |
| `payinMethodParam` | object |  |
| `scope` | string |  |
| `taxOnFees` | number |  |
| `transactionId` | string |  |
| `updatedAt` | string |  |
| `virtualAccountId` | string |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Finmo API, this operation is `POST /virtual-account` (base URL `https://api.finmo.net/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-virtual-account.md) for the provider-specific parameters and requirements.

