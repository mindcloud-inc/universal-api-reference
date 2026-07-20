# OxaPay Crypto Payment Gateway: List Payments

Retrieves payments from OxaPay.

```
GET https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/list-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OxaPay Crypto Payment Gateway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/list-payments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/list-payments?${params}`, {
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
| `page` | number | no | Page number. |
| `size` | number | no | Page size. |
| `track_id` | string | no | Filter by payment track id. |
| `type` | string | no | Filter by payment type. |
| `status` | string | no | Filter by payment status. |
| `pay_currency` | string | no | Filter by pay currency symbol. |
| `currency` | string | no | Filter by invoice currency symbol. |
| `network` | string | no | Filter by blockchain network. |
| `address` | string | no | Filter by destination address. |
| `from_date` | number | no | UNIX start timestamp. |
| `to_date` | number | no | UNIX end timestamp. |
| `from_amount` | number | no | Minimum amount filter. |
| `to_amount` | number | no | Maximum amount filter. |
| `sort_by` | string | no | Sort field. |
| `sort_type` | string | no | Sort direction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "list": [
          {
            "address": "string",
            "amount": 1,
            "currency": "string",
            "date": 1,
            "description": "string",
            "email": "ava@example.com",
            "expiredAt": 1,
            "network": "string",
            "orderId": "string",
            "payAmount": 1,
            "payCurrency": "string",
            "status": "string",
            "trackId": 1,
            "type": "string"
          }
        ],
        "meta": {
          "lastPage": 1,
          "page": 1,
          "total": 1
        }
      },
      "error": {},
      "message": "string",
      "status": 1,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Payment list response. |
| `data.list` | array<object> | Payments matching the current filters. |
| `data.list[].address` | string | Deposit address. |
| `data.list[].amount` | number | Requested amount. |
| `data.list[].currency` | string | Requested settlement currency. |
| `data.list[].date` | number | Creation timestamp. |
| `data.list[].description` | string | Merchant description. |
| `data.list[].email` | string | Customer email. |
| `data.list[].expiredAt` | number | Invoice expiration time. |
| `data.list[].network` | string | Blockchain network. |
| `data.list[].orderId` | string | Merchant order identifier. |
| `data.list[].payAmount` | number | Amount paid by the payer when available. |
| `data.list[].payCurrency` | string | Currency used by the payer when available. |
| `data.list[].status` | string | Current payment status. |
| `data.list[].trackId` | number | Payment track identifier. |
| `data.list[].type` | string | Payment type. |
| `data.meta` | object | Pagination metadata. |
| `data.meta.lastPage` | number | Last page number. |
| `data.meta.page` | number | Current page. |
| `data.meta.total` | number | Total matching payments. |
| `error` | object | Provider error payload when present. |
| `message` | string | Provider message. |
| `status` | number | HTTP-style status code. |
| `version` | string | Provider API version. |

## Native endpoint

Through the native OxaPay Crypto Payment Gateway API, this operation is `GET /payment` (base URL `https://api.oxapay.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payments.md) for the provider-specific parameters and requirements.

