# Finmei: List Invoices



```
GET https://connect.mindcloud.co/v1/universal/finmei/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finmei/latest/actions/list-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finmei/latest/actions/list-invoices?${params}`, {
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
        {
          "businessId": "string",
          "buyer": {
            "firstName": "Ava",
            "lastName": "Chen",
            "type": "string"
          },
          "createdAt": 1,
          "currency": "string",
          "id": "string",
          "invoiceDate": "string",
          "invoiceNumber": "string",
          "invoiceType": "string",
          "items": [
            {
              "name": "Ava Chen",
              "price": 1,
              "quantity": 1,
              "units": "string",
              "vatPercentage": 1
            }
          ],
          "paymentStatus": "string",
          "shareLink": "https://example.com",
          "totalInclVat": 1,
          "updatedAt": 1
        }
      ],
      "meta": {
        "currentPage": 1,
        "lastPage": 1,
        "path": "string",
        "perPage": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].businessId` | string |  |
| `data[].buyer.firstName` | string |  |
| `data[].buyer.lastName` | string |  |
| `data[].buyer.type` | string |  |
| `data[].createdAt` | number |  |
| `data[].currency` | string |  |
| `data[].id` | string |  |
| `data[].invoiceDate` | string |  |
| `data[].invoiceNumber` | string |  |
| `data[].invoiceType` | string |  |
| `data[].items` | array<object> |  |
| `data[].items[].name` | string |  |
| `data[].items[].price` | number |  |
| `data[].items[].quantity` | number |  |
| `data[].items[].units` | string |  |
| `data[].items[].vatPercentage` | number |  |
| `data[].paymentStatus` | string |  |
| `data[].shareLink` | string |  |
| `data[].totalInclVat` | number |  |
| `data[].updatedAt` | number |  |
| `meta.currentPage` | number |  |
| `meta.lastPage` | number |  |
| `meta.path` | string |  |
| `meta.perPage` | number |  |
| `meta.total` | number |  |

## Native endpoint

Through the native Finmei API, this operation is `GET /invoices` (base URL `https://app.finmei.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

