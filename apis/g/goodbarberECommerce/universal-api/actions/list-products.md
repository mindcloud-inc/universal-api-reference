# Goodbarber eCommerce: List Products



```
GET https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goodbarber eCommerce `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-products?${params}`, {
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
| `keyword` | string | no | Restricts the list of returned products to the ones whose title, summary, description, tags, SKU, or slug contains the provided argument. Use comma-separated values to match A OR B. |
| `status` | string | no | Restricts the list of returned products to a certain publishing status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "next": "string",
      "previous": "string",
      "products": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | <div class="field_description">Number of products returned by the API.</div> |
| `next` | string | <div class="field_description">URL to access the next page of the products list.</div> |
| `previous` | string | <div class="field_description">URL to access the previous page of the products list.</div> |
| `products` | array<object> | <div class="field_description">List of products.</div> |

## Native endpoint

Through the native Goodbarber eCommerce API, this operation is `GET /publicapi/v2/general/catalog/:webzine_id/product/` (base URL `https://commerce.goodbarber.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

