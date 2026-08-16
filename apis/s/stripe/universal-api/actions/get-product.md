# Stripe: Get Product



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/get-product?connectionId=$CONNECTION_ID&id=prod_..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "prod_..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/get-product?${params}`, {
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
| `id` | string | yes | The unique Stripe product ID. Example: `prod_...`. |

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

Through the native Stripe API, this operation is `GET products/:id` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

