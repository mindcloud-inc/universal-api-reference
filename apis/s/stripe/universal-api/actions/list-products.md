# Stripe: List Products



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-products?${params}`, {
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
| `active` | boolean | no | Only return products that are active or inactive. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `created` | object | no | Only return products created during a date interval. |
| `created.gt` | date | no | Minimum creation timestamp, exclusive. |
| `created.gte` | date | no | Minimum creation timestamp, inclusive. |
| `created.lt` | date | no | Maximum creation timestamp, exclusive. |
| `created.lte` | date | no | Maximum creation timestamp, inclusive. |
| `ids[]` | array<string> | no | Only return products with the given IDs. Accepts multiple values as an array. Example: `prod_...`. |
| `shippable` | boolean | no | Only return products that can be shipped. |
| `url` | string | no | Only return products with the given URL. Example: `https://example.com/product`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "created": 1,
      "defaultPrice": "string",
      "description": "string",
      "id": "string",
      "images": [
        "string"
      ],
      "livemode": true,
      "marketingFeatures": [
        {}
      ],
      "metadata": {},
      "name": "Ava Chen",
      "object": "string",
      "packageDimensions": {},
      "shippable": true,
      "statementDescriptor": "string",
      "taxCode": "string",
      "taxDetails": {},
      "type": "string",
      "unitLabel": "string",
      "updated": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the product is active |
| `created` | number | Creation timestamp in seconds |
| `defaultPrice` | string | Default price ID |
| `description` | string | Product description |
| `id` | string | Stripe product ID |
| `images` | array<string> | Product image URLs |
| `livemode` | boolean | Whether the product exists in live mode |
| `marketingFeatures` | array<object> | Product marketing features |
| `metadata` | object | Product metadata |
| `name` | string | Product name |
| `object` | string | Stripe object type |
| `packageDimensions` | object | Product package dimensions |
| `shippable` | boolean | Whether the product is shippable |
| `statementDescriptor` | string | Statement descriptor |
| `taxCode` | string | Tax code ID |
| `taxDetails` | object | Product tax details |
| `type` | string | Product type |
| `unitLabel` | string | Unit label |
| `updated` | number | Last update timestamp in seconds |
| `url` | string | Product URL |

## Native endpoint

Through the native Stripe API, this operation is `GET products` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

