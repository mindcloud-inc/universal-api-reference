# Visma eAccounting: List Orders

Retrieves all orders from Visma eAccounting.

```
GET https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Visma eAccounting `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/list-orders?${params}`, {
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
      "data": [
        [
          {}
        ]
      ],
      "meta": {
        "currentPage": 1,
        "pageSize": 1,
        "totalNumberOfPages": 1,
        "totalNumberOfResults": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<object> |  |
| `data[].amount` | number |  |
| `data[].currencyCode` | string |  |
| `data[].customerId` | string |  |
| `data[].customerName` | string |  |
| `data[].customerNumber` | string |  |
| `data[].deliveryDate` | date |  |
| `data[].id` | string |  |
| `data[].vatAmount` | number |  |
| `meta` | object |  |
| `meta.currentPage` | number |  |
| `meta.pageSize` | number |  |
| `meta.totalNumberOfPages` | number |  |
| `meta.totalNumberOfResults` | number |  |

## Native endpoint

Through the native Visma eAccounting API, this operation is `GET /orders` (base URL `https://eaccountingapi.vismaonline.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

