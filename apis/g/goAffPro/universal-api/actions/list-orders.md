# GoAffPro: List Orders

Retrieves a list of affiliate orders from GoAffPro.

```
GET https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-orders?connectionId=$CONNECTION_ID&fields%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fields[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-orders?${params}`, {
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
| `affiliateId` | string | no | Only return orders for this affiliate ID. |
| `customerEmail` | string | no | Only return orders for this customer email address. |
| `fields[]` | array<string> | yes | Fields to include in returned orders. |
| `status` | string | no | Only return orders with this status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliateId": 1,
      "commission": 1,
      "created": "string",
      "id": 1,
      "status": "string",
      "subtotal": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliateId` | number |  |
| `commission` | number |  |
| `created` | string |  |
| `id` | number | Order ID |
| `status` | string |  |
| `subtotal` | number |  |
| `total` | number |  |

## Native endpoint

Through the native GoAffPro API, this operation is `GET /admin/orders` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

