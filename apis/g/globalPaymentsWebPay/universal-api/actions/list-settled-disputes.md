# Global Payments WebPay: List Settled Disputes

Retrieves settled disputes from Global Payments WebPay.

```
GET https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/list-settled-disputes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Payments WebPay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/list-settled-disputes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/list-settled-disputes?${params}`, {
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
      "current_page_size": 1,
      "disputes": [
        {
          "amount": "string",
          "id": "string",
          "stage": "string",
          "status": "string"
        }
      ],
      "paging": {
        "page": 1,
        "page_size": 1
      },
      "total_record_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_page_size` | number |  |
| `disputes[].amount` | string |  |
| `disputes[].id` | string |  |
| `disputes[].stage` | string |  |
| `disputes[].status` | string |  |
| `paging.page` | number |  |
| `paging.page_size` | number |  |
| `total_record_count` | number |  |

## Native endpoint

Through the native Global Payments WebPay API, this operation is `GET /settlement/disputes` (base URL `https://apis.globalpay.com/ucp`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-settled-disputes.md) for the provider-specific parameters and requirements.

