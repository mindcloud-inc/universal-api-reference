# Gumroad: Get Payout

Retrieves a payout from Gumroad.

```
GET https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-payout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gumroad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-payout?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-payout?${params}`, {
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
| `id` | string | yes | The payout ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "payout": {
        "amount": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "currency": "string",
        "disputedSales": [
          [
            "string"
          ]
        ],
        "id": "string",
        "paymentProcessor": "string",
        "processedAt": "2026-05-07T12:00:00.000Z",
        "refundedSales": [
          [
            "string"
          ]
        ],
        "sales": [
          [
            "string"
          ]
        ],
        "status": "string",
        "transactions": [
          [
            {}
          ]
        ]
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `payout` | object |  |
| `payout.amount` | string |  |
| `payout.createdAt` | date |  |
| `payout.currency` | string |  |
| `payout.disputedSales[]` | array<string> |  |
| `payout.id` | string |  |
| `payout.paymentProcessor` | string |  |
| `payout.processedAt` | date |  |
| `payout.refundedSales[]` | array<string> |  |
| `payout.sales[]` | array<string> |  |
| `payout.status` | string |  |
| `payout.transactions[]` | array<object> |  |
| `payout.transactions[].buyerEmail` | string |  |
| `payout.transactions[].buyerName` | string |  |
| `payout.transactions[].date` | date |  |
| `payout.transactions[].itemName` | string |  |
| `payout.transactions[].netTotal` | number |  |
| `payout.transactions[].purchaseId` | string |  |
| `payout.transactions[].salePrice` | number |  |
| `payout.transactions[].type` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Gumroad API, this operation is `GET /payouts/:id` (base URL `https://api.gumroad.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payout.md) for the provider-specific parameters and requirements.

