# Visma eAccounting: Get Order

Retrieves an order from Visma eAccounting.

```
GET https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Visma eAccounting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/get-order?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/get-order?${params}`, {
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
      "amount": 1,
      "createdUtc": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "customerId": "string",
      "customerName": "Ava Chen",
      "customerNumber": "string",
      "deliveryDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "rows": [
        [
          {}
        ]
      ],
      "vatAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `createdUtc` | date |  |
| `currencyCode` | string |  |
| `customerId` | string |  |
| `customerName` | string |  |
| `customerNumber` | string |  |
| `deliveryDate` | date |  |
| `id` | string |  |
| `rows[]` | array<object> |  |
| `rows[].id` | string |  |
| `rows[].quantity` | number |  |
| `rows[].text` | string |  |
| `rows[].unitPrice` | number |  |
| `vatAmount` | number |  |

## Native endpoint

Through the native Visma eAccounting API, this operation is `GET /orders/{id}` (base URL `https://eaccountingapi.vismaonline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

