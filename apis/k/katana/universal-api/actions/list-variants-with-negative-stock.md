# Katana: List Variants with Negative Stock

Lists variants with negative stock in Katana.

```
GET https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-variants-with-negative-stock
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-variants-with-negative-stock?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-variants-with-negative-stock?${params}`, {
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
| `locationId` | number | no | Filters negative stock by a valid location id |
| `variantId` | number | no | Filters negative stock by a valid variant id |
| `latestNegativeStockDateMax` | string | no | Filters negative stock by a latest negative stock date max |
| `latestNegativeStockDateMin` | string | no | Filters negative stock by a latest negative stock date min |
| `name` | string | no | Filters negative stock by a name |
| `sku` | string | no | Filters negative stock by a sku |
| `category` | string | no | Filters negative stock by a category |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "latestNegativeStockDate": "string",
      "locationId": 1,
      "name": "Ava Chen",
      "sku": "string",
      "variantId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `latestNegativeStockDate` | string |  |
| `locationId` | number |  |
| `name` | string |  |
| `sku` | string |  |
| `variantId` | number |  |

## Native endpoint

Through the native Katana API, this operation is `GET /negative_stock` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-variants-with-negative-stock.md) for the provider-specific parameters and requirements.

