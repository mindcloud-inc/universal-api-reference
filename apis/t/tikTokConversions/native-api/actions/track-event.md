# Track Event with TikTok Conversions

Reports a web event to TikTok Conversions.

## Endpoint

- **Method:** `POST`
- **Path:** `/open_api/v1.3/event/track/`
- **Base URL:** `https://business-api.tiktok.com`
- **Official documentation:** [Track Event](https://business-api.tiktok.com/portal/docs?id=1771101303285761)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `test_event_code` | body | `string` | no | Optional TikTok test event code for non-production validation. |
| `data[].event` | body | `string` | yes | Standard or custom TikTok event name. |
| `data[].event_time` | body | `number` | yes | Unix timestamp in seconds for when the event occurred. |
| `data[].event_id` | body | `string` | no | Optional deduplication identifier shared with Pixel events. |
| `data[].limited_data_use` | body | `boolean` | no | Optional limited data use flag. |
| `data[].user.email` | body | `string` | no | User email. TikTok recommends SHA-256 hashing when applicable. |
| `data[].user.phone` | body | `string` | no | User phone number. TikTok recommends SHA-256 hashing when applicable. |
| `data[].user.external_id` | body | `string` | no | Advertiser-defined customer identifier. |
| `data[].user.ttclid` | body | `string` | no | TikTok click identifier from the landing URL. |
| `data[].user.ttp` | body | `string` | no | TikTok first-party cookie value. |
| `data[].user.ip` | body | `string` | no | Client IP address. |
| `data[].user.user_agent` | body | `string` | no | Client user agent string. |
| `data[].properties.currency` | body | `string` | no | ISO currency code for the event value. |
| `data[].properties.value` | body | `number` | no | Monetary value for the event. |
| `data[].properties.content_type` | body | `string` | no | TikTok content type, such as product or product_group. |
| `data[].properties.query` | body | `string` | no | Search query associated with the event. |
| `data[].properties.description` | body | `string` | no | Description associated with the tracked event. |
| `data[].properties.contents[].price` | body | `number` | no | Item price. |
| `data[].properties.contents[].quantity` | body | `number` | no | Item quantity. |
| `data[].properties.contents[].content_id` | body | `string` | no | Catalog or product identifier. |
| `data[].properties.contents[].content_category` | body | `string` | no | Category for the content item. |
| `data[].properties.contents[].content_name` | body | `string` | no | Name of the content item. |
| `data[].properties.contents[].brand` | body | `string` | no | Brand associated with the content item. |
| `data[].page.url` | body | `string` | no | URL of the page where the event occurred. |
| `data[].page.referrer` | body | `string` | no | Referrer URL for the page view. |
