# Ontraport: List Transactions

Retrieves a list of transactions from Ontraport.

```
GET https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ontraport `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/list-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/list-transactions?${params}`, {
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
      "balance": "string",
      "bindex": "string",
      "ccId": "string",
      "city": "string",
      "closedDate": "2026-05-07T12:00:00.000Z",
      "contactId": "string",
      "contactName": "Ava Chen",
      "county": "string",
      "currency": "string",
      "customerNote": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "dlm": "2026-05-07T12:00:00.000Z",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "externalOrderId": "string",
      "formId": "string",
      "gatewayId": "string",
      "hasRefunded": "string",
      "hidden": "string",
      "id": "string",
      "internalNote": "string",
      "invoiceDate": "2026-05-07T12:00:00.000Z",
      "lastRechargeDate": "2026-05-07T12:00:00.000Z",
      "lpId": "string",
      "oprid": "string",
      "orderId": "string",
      "origTransAmount": "string",
      "owner": "string",
      "recharge": "string",
      "rechargeAttempts": "string",
      "shipping": "string",
      "state": "string",
      "status": "string",
      "stripeTaxCalculationId": "string",
      "stripeTaxTransactionId": "string",
      "subtotal": "string",
      "tax": "string",
      "taxCity": "string",
      "taxCounty": "string",
      "taxState": "string",
      "templateId": "string",
      "total": "string",
      "totalPaid": "string",
      "type": "string",
      "uniqueId": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | string |  |
| `bindex` | string |  |
| `ccId` | string |  |
| `city` | string |  |
| `closedDate` | date |  |
| `contactId` | string |  |
| `contactName` | string |  |
| `county` | string |  |
| `currency` | string |  |
| `customerNote` | string |  |
| `date` | date |  |
| `dlm` | date |  |
| `dueDate` | date |  |
| `externalOrderId` | string |  |
| `formId` | string |  |
| `gatewayId` | string |  |
| `hasRefunded` | string |  |
| `hidden` | string |  |
| `id` | string |  |
| `internalNote` | string |  |
| `invoiceDate` | date |  |
| `lastRechargeDate` | date |  |
| `lpId` | string |  |
| `oprid` | string |  |
| `orderId` | string |  |
| `origTransAmount` | string |  |
| `owner` | string |  |
| `recharge` | string |  |
| `rechargeAttempts` | string |  |
| `shipping` | string |  |
| `state` | string |  |
| `status` | string |  |
| `stripeTaxCalculationId` | string |  |
| `stripeTaxTransactionId` | string |  |
| `subtotal` | string |  |
| `tax` | string |  |
| `taxCity` | string |  |
| `taxCounty` | string |  |
| `taxState` | string |  |
| `templateId` | string |  |
| `total` | string |  |
| `totalPaid` | string |  |
| `type` | string |  |
| `uniqueId` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native Ontraport API, this operation is `GET /Transactions` (base URL `https://api.ontraport.com/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

