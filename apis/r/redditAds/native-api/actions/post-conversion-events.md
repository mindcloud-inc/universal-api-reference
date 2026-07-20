# Post Conversion Events with Reddit Lead Ads

Creates conversion events for a Reddit pixel.

## Endpoint

- **Method:** `POST`
- **Path:** `/pixels/{pixel_id}/conversion_events`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [Post Conversion Events](https://ads-api.reddit.com/docs/v3/operations/post-conversion-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pixel_id` | path | `string` | yes | Reddit Ads pixel identifier. |
| `data` | body | `object` | yes | JSON request body from the Reddit Ads API spec. |
