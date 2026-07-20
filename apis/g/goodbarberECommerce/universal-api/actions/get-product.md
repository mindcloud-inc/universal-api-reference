# Goodbarber eCommerce: Get Product



```
GET https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goodbarber eCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-product?connectionId=$CONNECTION_ID&productId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-product?${params}`, {
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
| `productId` | number | yes | Product Unique ID. Default: `1`. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auto_similar_products": [
        {}
      ],
      "brand": "string",
      "collections": [
        1
      ],
      "created_at": "string",
      "custom_similar_products": [
        {}
      ],
      "description": {},
      "highlight": true,
      "id": 1,
      "media": 1,
      "meta_description": "string",
      "meta_title": "string",
      "pdf": "string",
      "pdf_name": "Ava Chen",
      "product_ref": "string",
      "show_similar_products": true,
      "slides": [
        {}
      ],
      "slug": "string",
      "status": "string",
      "summary": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "updated_at": "string",
      "variants": [
        {}
      ],
      "visibility_end": "string",
      "visibility_start": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auto_similar_products` | array<object> | <div class="field_description">Automatically generated list containing products similar to the current instance.<br>The list is created from all the available products of the shop, based on criterias such as tags and collections.</div> |
| `brand` | string | <div class="field_description">Product brand platform.</div> |
| `collections` | array<number> | <div class="field_description">List of the collections (unique IDs) to which the product belongs.</div> |
| `created_at` | string | <div class="field_description">Timestamp of the product creation.</div> |
| `custom_similar_products` | array<object> | <div class="field_description">Manually defined list of similar products.</div> |
| `description` | object |  |
| `highlight` | boolean | <div class="field_description">Boolean indicating if the product should be showcased in the shop products list or not.</div> |
| `id` | number | <div class="field_description">Product unique ID.</div> |
| `media` | number | <div class="field_description">Unique ID of the slide selected as the product thumbnail.</div> |
| `meta_description` | string | <div class="field_description">Product SEO description (for referencing by search engines).</div> |
| `meta_title` | string | <div class="field_description">Product SEO title (for referencing by search engines).</div> |
| `pdf` | string | <div class="field_description">URL of the PDF file uploaded for this product.</div> |
| `pdf_name` | string | <div class="field_description">Name of the PDF file associated with the product.</div> |
| `product_ref` | string | <div class="field_description">Product reference ID.</div> |
| `show_similar_products` | boolean | <div class="field_description">Boolean indicating whether the "Similar products" section should be displayed in the shop for this product or not.</div> |
| `slides` | array<object> | <div class="field_description">Set of slides (pictures) associated with the product.</div> |
| `slug` | string | <div class="field_description">Product slug (used in its access URL).</div> |
| `status` | string |  |
| `summary` | string | <div class="field_description">Product short description.</div> |
| `tags` | array<string> | <div class="field_description">Set of tags associated with the product.</div> |
| `title` | string | <div class="field_description">Product name.</div> |
| `updated_at` | string | <div class="field_description">Timestamp of the product last update.</div> |
| `variants` | array<object> | <div class="field_description">Product variants list.</div> |
| `visibility_end` | string | <div class="field_description">Datetime <strong>until which</strong> the product should be visible to the customers.<br>If this field is <code>null</code>, the product will remain visible in the shop until it gets manually hidden or removed.</div> |
| `visibility_start` | string | <div class="field_description">Datetime <strong>from which</strong> the product should become visible to the customers.<br>If this field is <code>null</code>, the product will directly become visible when its status is set to <code>"PUBLISHED"</code>.</div> |

## Native endpoint

Through the native Goodbarber eCommerce API, this operation is `GET /publicapi/v2/general/catalog/:webzine_id/product/:product_id/` (base URL `https://commerce.goodbarber.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

