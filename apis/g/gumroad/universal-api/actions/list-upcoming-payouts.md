# Gumroad: List Upcoming Payouts

Retrieves upcoming payouts from Gumroad.

```
GET https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/list-upcoming-payouts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gumroad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/list-upcoming-payouts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/list-upcoming-payouts?${params}`, {
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
| `includeSales` | boolean | no | Set to false to exclude sales details from the response. |
| `includeTransactions` | boolean | no | Set to true to include payout transaction details. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "payouts": [
        [
          {}
        ]
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `payouts[]` | array<object> |  |
| `payouts[].amount` | string |  |
| `payouts[].createdAt` | date |  |
| `payouts[].currency` | string |  |
| `payouts[].disputedSales[]` | array<string> |  |
| `payouts[].id` | string |  |
| `payouts[].paymentProcessor` | string |  |
| `payouts[].processedAt` | date |  |
| `payouts[].refundedSales[]` | array<string> |  |
| `payouts[].sales[]` | array<string> |  |
| `payouts[].status` | string |  |
| `payouts[].transactions[]` | array<object> |  |
| `payouts[].transactions[].buyerEmail` | string |  |
| `payouts[].transactions[].buyerName` | string |  |
| `payouts[].transactions[].date` | date |  |
| `payouts[].transactions[].itemName` | string |  |
| `payouts[].transactions[].netTotal` | number |  |
| `payouts[].transactions[].purchaseId` | string |  |
| `payouts[].transactions[].salePrice` | number |  |
| `payouts[].transactions[].type` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Gumroad API, this operation is `GET /payouts/upcoming` (base URL `https://api.gumroad.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-upcoming-payouts.md) for the provider-specific parameters and requirements.

