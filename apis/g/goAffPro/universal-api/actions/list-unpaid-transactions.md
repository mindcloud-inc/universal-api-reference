# GoAffPro: List Unpaid Transactions

Retrieves unpaid affiliate transactions from GoAffPro.

```
GET https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-unpaid-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-unpaid-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-unpaid-transactions?${params}`, {
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
| `affiliateId` | string | no | Only return unpaid transactions for this affiliate ID. |
| `groupId` | string | no | Only return unpaid transactions for this group ID. |
| `paymentMethod` | string | no | Only return unpaid transactions with this payment method. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliateId": 1,
      "amount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "entityId": 1,
      "entityType": "string",
      "eventType": "string",
      "txId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliateId` | number |  |
| `amount` | number |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `entityId` | number |  |
| `entityType` | string |  |
| `eventType` | string |  |
| `txId` | number |  |

## Native endpoint

Through the native GoAffPro API, this operation is `GET /admin/payments/transactions/unpaid` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unpaid-transactions.md) for the provider-specific parameters and requirements.

