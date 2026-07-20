# Recurly: List Transactions



```
GET https://connect.mindcloud.co/v1/universal/recurly/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recurly `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recurly/latest/actions/list-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recurly/latest/actions/list-transactions?${params}`, {
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
| `beginTime` | string | no |  |
| `endTime` | string | no |  |
| `ids` | string | no |  |
| `success` | boolean | no |  |
| `type` | string | no | One of: `0`, `1`, `2`, `3`, `4`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {},
      "actionResult": {},
      "amount": 1,
      "avsCheck": "string",
      "backupPaymentMethodUsed": true,
      "billingAddress": {},
      "collectedAt": "2026-05-07T12:00:00.000Z",
      "collectionMethod": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customerMessage": "string",
      "customerMessageLocale": "string",
      "cvvCheck": "string",
      "fraudInfo": {},
      "gatewayApprovalCode": "string",
      "gatewayMessage": "string",
      "gatewayReference": "string",
      "gatewayResponseCode": "string",
      "gatewayResponseTime": 1,
      "gatewayResponseValues": {},
      "id": "string",
      "initiator": {},
      "invoice": {},
      "ipAddressCountry": "string",
      "ipAddressV4": "string",
      "merchantReasonCode": "string",
      "nextAction": {},
      "object": "string",
      "origin": "string",
      "originalTransactionId": "string",
      "paymentGateway": {},
      "paymentMethod": {},
      "refunded": true,
      "status": "string",
      "statusCode": "string",
      "statusMessage": "string",
      "subscriptionIds": [
        "string"
      ],
      "success": true,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string",
      "vatNumber": "string",
      "voidedAt": "2026-05-07T12:00:00.000Z",
      "voidedByInvoice": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `actionResult` | object |  |
| `amount` | number |  |
| `avsCheck` | string |  |
| `backupPaymentMethodUsed` | boolean |  |
| `billingAddress` | object |  |
| `collectedAt` | date |  |
| `collectionMethod` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `customerMessage` | string |  |
| `customerMessageLocale` | string |  |
| `cvvCheck` | string |  |
| `fraudInfo` | object |  |
| `gatewayApprovalCode` | string |  |
| `gatewayMessage` | string |  |
| `gatewayReference` | string |  |
| `gatewayResponseCode` | string |  |
| `gatewayResponseTime` | number |  |
| `gatewayResponseValues` | object |  |
| `id` | string |  |
| `initiator` | object |  |
| `invoice` | object |  |
| `ipAddressCountry` | string |  |
| `ipAddressV4` | string |  |
| `merchantReasonCode` | string |  |
| `nextAction` | object |  |
| `object` | string |  |
| `origin` | string |  |
| `originalTransactionId` | string |  |
| `paymentGateway` | object |  |
| `paymentMethod` | object |  |
| `refunded` | boolean |  |
| `status` | string |  |
| `statusCode` | string |  |
| `statusMessage` | string |  |
| `subscriptionIds` | array<string> |  |
| `success` | boolean |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |
| `vatNumber` | string |  |
| `voidedAt` | date |  |
| `voidedByInvoice` | object |  |

## Native endpoint

Through the native Recurly API, this operation is `GET /transactions` (base URL `https://v3.recurly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

