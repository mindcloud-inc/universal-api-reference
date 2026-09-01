# Zenoti: List Purchases By Guest



```
GET https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-purchases-by-guest
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenoti `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-purchases-by-guest?connectionId=$CONNECTION_ID&limit=25&offset=0&guestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "guestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-purchases-by-guest?${params}`, {
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
| `guestId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balanceQuantity": 1,
      "center": {
        "id": "string",
        "name": "Ava Chen"
      },
      "discount": 1,
      "id": "string",
      "invoice": {
        "id": "string",
        "invoiceItemId": "string",
        "invoiceNumber": "string",
        "receiptNumber": "string",
        "source": 1,
        "status": "string"
      },
      "name": "Ava Chen",
      "paymentType": "string",
      "price": 1,
      "pricePaid": 1,
      "promotion": "string",
      "quantity": 1,
      "saleBy": "Ava Chen",
      "saleDate": "2026-05-07T12:00:00.000Z",
      "taxes": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balanceQuantity` | number |  |
| `center.id` | string |  |
| `center.name` | string |  |
| `discount` | number |  |
| `id` | string |  |
| `invoice.id` | string |  |
| `invoice.invoiceItemId` | string |  |
| `invoice.invoiceNumber` | string |  |
| `invoice.receiptNumber` | string |  |
| `invoice.source` | number |  |
| `invoice.status` | string |  |
| `name` | string |  |
| `paymentType` | string |  |
| `price` | number |  |
| `pricePaid` | number |  |
| `promotion` | string |  |
| `quantity` | number |  |
| `saleBy` | string |  |
| `saleDate` | date |  |
| `taxes` | number |  |

## Native endpoint

Through the native Zenoti API, this operation is `GET guests/:guestId/products` (base URL `https://api.zenoti.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-purchases-by-guest.md) for the provider-specific parameters and requirements.

