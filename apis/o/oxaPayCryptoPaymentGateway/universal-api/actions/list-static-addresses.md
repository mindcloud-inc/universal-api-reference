# OxaPay Crypto Payment Gateway: List Static Addresses

Retrieves static addresses from OxaPay.

```
GET https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/list-static-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OxaPay Crypto Payment Gateway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/list-static-addresses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/list-static-addresses?${params}`, {
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
| `track_id` | string | no | Filter by static address track id. |
| `order_id` | string | no | Filter by merchant order id. |
| `email` | string | no | Filter by customer email. |
| `have_tx` | boolean | no | Filter static addresses with transactions. |
| `currency` | string | no | Filter by currency symbol. |
| `network` | string | no | Filter by blockchain network. |
| `address` | string | no | Filter by static address. |

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
            "callbackUrl": "https://example.com",
            "date": 1,
            "description": "string",
            "email": "ava@example.com",
            "memo": "string",
            "network": "string",
            "orderId": "string",
            "trackId": 1
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
| `data` | object | Static-address list response. |
| `data.list` | array<object> | Static addresses matching the current filters. |
| `data.list[].address` | string | Static deposit address. |
| `data.list[].callbackUrl` | string | Webhook callback URL. |
| `data.list[].date` | number | Creation timestamp. |
| `data.list[].description` | string | Merchant description. |
| `data.list[].email` | string | Customer email. |
| `data.list[].memo` | string | Memo or destination tag when provided. |
| `data.list[].network` | string | Blockchain network. |
| `data.list[].orderId` | string | Merchant order identifier. |
| `data.list[].trackId` | number | Static-address track identifier. |
| `data.meta` | object | Pagination metadata. |
| `data.meta.lastPage` | number | Last page number. |
| `data.meta.page` | number | Current page. |
| `data.meta.total` | number | Total matching static addresses. |
| `error` | object | Provider error payload when present. |
| `message` | string | Provider message. |
| `status` | number | HTTP-style status code. |
| `version` | string | Provider API version. |

## Native endpoint

Through the native OxaPay Crypto Payment Gateway API, this operation is `GET /payment/static-address` (base URL `https://api.oxapay.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-static-addresses.md) for the provider-specific parameters and requirements.

