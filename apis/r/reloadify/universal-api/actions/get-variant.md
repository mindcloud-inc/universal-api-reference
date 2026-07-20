# Reloadify: Get Variant

Retrieves a product variant from Reloadify.

```
GET https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-variant?connectionId=$CONNECTION_ID&language_id=string&variant_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "language_id": "string",
  "variant_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-variant?${params}`, {
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
| `language_id` | string | yes | Language ID from the Reloadify language resource. |
| `variant_id` | string | yes | Variant ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "article_code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "default": true,
      "ean": "string",
      "id": "string",
      "main_image": "string",
      "old_price_excl": 1,
      "old_price_incl": 1,
      "price_cost": 1,
      "price_excl": 1,
      "price_incl": 1,
      "product_id": "string",
      "sku": "string",
      "stock_level": 1,
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `article_code` | string |  |
| `created_at` | date |  |
| `default` | boolean |  |
| `ean` | string |  |
| `id` | string |  |
| `main_image` | string |  |
| `old_price_excl` | number |  |
| `old_price_incl` | number |  |
| `price_cost` | number |  |
| `price_excl` | number |  |
| `price_incl` | number |  |
| `product_id` | string |  |
| `sku` | string |  |
| `stock_level` | number |  |
| `title` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Reloadify API, this operation is `GET /v2/languages/:language_id/variants/:variant_id` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-variant.md) for the provider-specific parameters and requirements.

