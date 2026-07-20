# RO App: List Invoice Items



```
GET https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-invoice-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-invoice-items?connectionId=$CONNECTION_ID&invoiceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-invoice-items?${params}`, {
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
| `invoiceId` | number | yes | Invoice ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "id": 1,
      "orderId": 1,
      "price": 1,
      "service": true,
      "title": "string",
      "type": 1,
      "uomId": 1,
      "warranty": 1,
      "warrantyPeriod": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `id` | number |  |
| `orderId` | number |  |
| `price` | number |  |
| `service` | boolean |  |
| `title` | string |  |
| `type` | number |  |
| `uomId` | number |  |
| `warranty` | number |  |
| `warrantyPeriod` | number |  |

## Native endpoint

Through the native RO App API, this operation is `GET /invoices/:invoice_id/items` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoice-items.md) for the provider-specific parameters and requirements.

