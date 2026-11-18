# Brightpearl: List Product Availability



```
GET https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-product-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brightpearl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-product-availability?connectionId=$CONNECTION_ID&productIds=100-120%2C130" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productIds": "100-120,130"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-product-availability?${params}`, {
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
| `productIds` | string | yes | A single ID, comma-separated IDs, or ranges. Example: `100-120,130`. |
| `includeOptional` | list<string> | no | One of: `allocatedOrders`, `allocatedTransfers`, `breakDownByLocation`, `onOrder`. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allocatedToOrders": {},
      "allocatedToTransfers": {},
      "id": 1,
      "total": {
        "allocated": 1,
        "inStock": 1,
        "inTransit": 1,
        "onHand": 1,
        "onOrder": {
          "shipped": 1,
          "total": 1
        }
      },
      "warehouses": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allocatedToOrders` | object |  |
| `allocatedToTransfers` | object |  |
| `id` | number |  |
| `total` | object |  |
| `total.allocated` | number |  |
| `total.inStock` | number |  |
| `total.inTransit` | number |  |
| `total.onHand` | number |  |
| `total.onOrder` | object |  |
| `total.onOrder.shipped` | number |  |
| `total.onOrder.total` | number |  |
| `warehouses` | object |  |

## Native endpoint

Through the native Brightpearl API, this operation is `GET /warehouse-service/product-availability/:productIds` (base URL `https://{{credentials.apiDomain}}/public-api/{{credentials.account}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-product-availability.md) for the provider-specific parameters and requirements.

