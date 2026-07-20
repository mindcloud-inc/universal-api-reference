# Finmo: Delete Virtual Account

Deletes an existing virtual account from Finmo.

```
DELETE https://connect.mindcloud.co/v1/universal/finmo/latest/actions/delete-virtual-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/delete-virtual-account?connectionId=$CONNECTION_ID&virtualAccountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "virtualAccountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finmo/latest/actions/delete-virtual-account?${params}`, {
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
| `virtualAccountId` | string | yes | Virtual account identifier to delete. |

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

Through the native Finmo API, this operation is `DELETE /virtual-account/:virtual_account_id` (base URL `https://api.finmo.net/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-virtual-account.md) for the provider-specific parameters and requirements.

