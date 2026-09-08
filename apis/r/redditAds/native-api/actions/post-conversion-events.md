# Post Conversion Events with Reddit Ads

Creates conversion events for a Reddit pixel.

## Endpoint

- **Method:** `POST`
- **Path:** `/pixels/:pixel_id/conversion_events`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [Post Conversion Events](https://ads-api.reddit.com/docs/v3/operations/post-conversion-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pixel_id` | path | `string` | yes | Reddit Ads pixel identifier. |
| `data` | body | `object` | yes | JSON request body from the Reddit Ads API spec. |
| `data.test_id` | body | `string` | no | Optional Reddit Events Manager test ID. Leave blank for production events. |
| `data.events[]` | body | `array<object>` | yes | One or more conversion events; Reddit accepts up to 1,000 events per request. |
| `data.events[].event_at` | body | `date` | yes | Unix epoch timestamp in milliseconds when the conversion occurred. |
| `data.events[].action_source` | body | `list<string>` | yes | Channel where the conversion occurred. Accepted values: `APP`, `OTHER`, `PHYSICAL_STORE`, `WEBSITE`. |
| `data.events[].type` | body | `object` | yes | — |
| `data.events[].type.tracking_type` | body | `list<string>` | yes | Reddit standard conversion type, or CUSTOM for a custom event. Accepted values: `ADD_TO_CART`, `ADD_TO_WISHLIST`, `CUSTOM`, `LEAD`, `PAGE_VISIT`, `PURCHASE`, `SEARCH`, `SIGN_UP`, `VIEW_CONTENT`. |
| `data.events[].type.custom_event_name` | body | `string` | no | Enter a name when Conversion Event is Custom, for example DemoBooked or TrialStarted. Leave blank for standard Reddit events. |
| `data.events[].click_id` | body | `string` | no | Reddit click ID (`rdt_cid`) used to improve attribution. |
| `data.events[].event_source_url` | body | `string` | no | URL where a WEBSITE conversion occurred; include `rdt_cid` when available. |
| `data.events[].metadata` | body | `object` | no | Optional conversion metadata used for deduplication and revenue reporting. |
| `data.events[].metadata.conversion_id` | body | `string` | no | Unique event ID used to deduplicate Pixel and CAPI events. |
| `data.events[].metadata.currency` | body | `string` | no | ISO 4217 currency code for revenue-related events. |
| `data.events[].metadata.value` | body | `number` | no | Transaction value in the currency's base unit. |
| `data.events[].metadata.item_count` | body | `number` | no | Total number of items for a revenue-related event. |
