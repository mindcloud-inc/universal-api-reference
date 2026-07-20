# ChargeDesk: Retrieve Product

Retrieves a product from ChargeDesk.

```
GET https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/retrieve-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/retrieve-product?connectionId=$CONNECTION_ID&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/retrieve-product?${params}`, {
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
| `productId` | string | yes | Product ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "amount_formatted": "string",
      "chargeable": "string",
      "company": "string",
      "currency": "string",
      "description": "string",
      "first_seen": 1,
      "interval": "string",
      "interval_count": "string",
      "name": "Ava Chen",
      "object": "string",
      "product_id": "string",
      "quantity": "string",
      "status": "string",
      "support_url": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `amount_formatted` | string |  |
| `chargeable` | string |  |
| `company` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `first_seen` | number |  |
| `interval` | string |  |
| `interval_count` | string |  |
| `name` | string |  |
| `object` | string |  |
| `product_id` | string |  |
| `quantity` | string |  |
| `status` | string |  |
| `support_url` | string |  |
| `url` | string |  |

## Native endpoint

Through the native ChargeDesk API, this operation is `GET /products/:PRODUCT_ID` (base URL `https://api.chargedesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-product.md) for the provider-specific parameters and requirements.

