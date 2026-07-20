# Create Pin with Pinterest

Creates a new pin in Pinterest.

## Endpoint

- **Method:** `POST`
- **Path:** `pins`
- **Base URL:** `https://api.pinterest.com/v5`
- **Official documentation:** [Create Pin](https://developers.pinterest.com/docs/api/v5/#operation/pins/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `alt_text` | body | `string` | no |
| `board_id` | body | `list` | no |
| `board_section_id` | body | `string` | no |
| `description` | body | `string` | no |
| `dominant_color` | body | `string` | no |
| `link` | body | `string` | no |
| `note` | body | `string` | no |
| `parent_pin_id` | body | `string` | no |
| `title` | body | `string` | no |
| `alt_text` | body | `string` | no |
| `media_source.items[].title` | body | `string` | no |
| `media_source.source_type` | body | `list` | no |
| `mediasource.items[].title` | body | `string` | no |
| `mediasource.source_type` | body | `list` | no |
| `product_link` | body | `string` | no |
| `product.price.currency` | body | `string` | no |
| `carouselSlides[].title` | body | `string` | no |
| `media_source.items[]` | body | `array` | no |
| `media_source.items[].content_type` | body | `string` | no |
| `mediasource.items[]` | body | `array` | no |
| `mediasource.items[].description` | body | `string` | no |
| `product_id` | body | `string` | no |
| `product.price.amount` | body | `string` | no |
| `carouselSlides[].description` | body | `string` | no |
| `media_source.items[].data` | body | `string` | no |
| `mediasource.items[].link` | body | `string` | no |
| `product.price` | body | `object` | no |
| `media_source.items[].link` | body | `string` | no |
| `mediasource.items[].url` | body | `string` | no |
| `product.availability` | body | `string` | no |
| `item_group_id` | body | `string` | no |
| `media_source.items[].description` | body | `string` | no |
| `mediasource.items[].index` | body | `string` | no |
| `media_source.items[].url` | body | `string` | no |
| `media_source` | body | `object` | no |
