# Global Payments WebPay: Search Payment Methods

Finds payment methods in Global Payments WebPay by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/search-payment-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Payments WebPay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/search-payment-methods?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/search-payment-methods?${params}`, {
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
      "account_id": "string",
      "current_page_size": 1,
      "merchant_id": "string",
      "payment_methods": [
        {
          "id": "string",
          "name": "Ava Chen",
          "reference": "string",
          "status": "string"
        }
      ],
      "total_record_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | string |  |
| `current_page_size` | number |  |
| `merchant_id` | string |  |
| `payment_methods[].id` | string |  |
| `payment_methods[].name` | string |  |
| `payment_methods[].reference` | string |  |
| `payment_methods[].status` | string |  |
| `total_record_count` | number |  |

## Native endpoint

Through the native Global Payments WebPay API, this operation is `POST /payment-methods/search` (base URL `https://apis.globalpay.com/ucp`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-payment-methods.md) for the provider-specific parameters and requirements.

