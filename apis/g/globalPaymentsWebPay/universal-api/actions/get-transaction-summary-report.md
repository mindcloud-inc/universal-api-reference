# Global Payments WebPay: Get Transaction Summary Report

Retrieves a transaction summary report from Global Payments WebPay.

```
GET https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/get-transaction-summary-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Payments WebPay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/get-transaction-summary-report?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/get-transaction-summary-report?${params}`, {
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
      "account_name": "Ava Chen",
      "current_page_size": 1,
      "merchant_id": "string",
      "paging": {
        "page": 1,
        "page_size": 1
      },
      "reports": [
        {
          "summary": {
            "sales": {
              "amount": "string",
              "count": 1
            }
          },
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_name` | string |  |
| `current_page_size` | number |  |
| `merchant_id` | string |  |
| `paging.page` | number |  |
| `paging.page_size` | number |  |
| `reports[].summary.sales.amount` | string |  |
| `reports[].summary.sales.count` | number |  |
| `reports[].type` | string |  |

## Native endpoint

Through the native Global Payments WebPay API, this operation is `GET /reports` (base URL `https://apis.globalpay.com/ucp`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-transaction-summary-report.md) for the provider-specific parameters and requirements.

