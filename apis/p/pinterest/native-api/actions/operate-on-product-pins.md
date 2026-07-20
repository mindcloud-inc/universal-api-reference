# Operate On Product Pins with Pinterest

Operates on Pinterest catalog items in batch.

## Endpoint

- **Method:** `POST`
- **Path:** `catalogs/items/batch`
- **Base URL:** `https://api.pinterest.com/v5`
- **Official documentation:** [Operate On Product Pins](https://developers.pinterest.com/docs/api/v5/#operation/items_batch/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `items[].attributes.shipping` | body | `string` | no |
| `items[].attributes.shipping_height` | body | `string` | no |
| `items[].attributes.shipping_weight` | body | `string` | no |
| `items[].attributes.shipping_width` | body | `string` | no |
| `items[].attributes.size` | body | `string` | no |
| `items[].attributes.size_system` | body | `string` | no |
| `items[].attributes.tax` | body | `string` | no |
| `items[].attributes.title` | body | `string` | no |
| `items[].attributes.variant_names` | body | `string` | no |
| `items[].attributes.variant_values` | body | `string` | no |
| `ad_account_id` | query | `string` | no |
| `items[].attributes.image_link` | body | `object<string>` | no |
| `items[].operation` | body | `list` | no |
| `catalog_type` | body | `list` | no |
| `items[].attributes` | body | `object` | no |
| `items[].attributes.video_link` | body | `string` | no |
| `country` | body | `string` | no |
| `items[].attributes.additional_image_link` | body | `object<string>` | no |
| `items[].item_id` | body | `string` | no |
| `items[].attributes.ad_link` | body | `string` | no |
| `language` | body | `string` | no |
| `items[]` | body | `array` | no |
| `items[].attributes.adult` | query | `string` | no |
| `items[].attributes.age_group` | body | `string` | no |
| `items[].attributes.availability` | body | `string` | no |
| `items[].attributes.average_review_rating` | body | `string` | no |
| `items[].attributes.brand` | body | `string` | no |
| `items[].attributes.color` | body | `string` | no |
| `items[].attributes.condition` | body | `string` | no |
| `items[].attributes.custom_label_0` | body | `string` | no |
| `items[].attributes.custom_label_1` | body | `string` | no |
| `items[].attributes.custom_label_3` | body | `string` | no |
| `items[].attributes.custom_label_2` | body | `string` | no |
| `items[].attributes.custom_label_4` | body | `string` | no |
| `items[].attributes.custom_label_5` | body | `string` | no |
| `items[].attributes.description` | body | `string` | no |
| `items[].attributes.free_shipping_label` | body | `string` | no |
| `items[].attributes.free_shipping_limit` | body | `string` | no |
| `items[].attributes.gender` | body | `string` | no |
| `items[].attributes.google_product_category` | body | `string` | no |
| `items[].attributes.gtin` | body | `string` | no |
| `items[].attributes.item_group_id` | body | `string` | no |
| `items[].attributes.last_update_time` | body | `string` | no |
| `items[].attributes.link` | body | `string` | no |
| `items[].attributes.material` | body | `string` | no |
| `items[].attributes.minimum_ad_price` | body | `string` | no |
| `items[].attributes.mobile_link` | body | `string` | no |
| `items[].attributes.mpn` | body | `string` | no |
| `items[].attributes.number_of_ratings` | body | `string` | no |
| `items[].attributes.number_of_reviews` | body | `string` | no |
| `items[].attributes.pattern` | body | `string` | no |
| `items[].attributes.price` | body | `string` | no |
| `items[].attributes.product_type` | body | `string` | no |
| `items[].attributes.sale_price` | body | `string` | no |
