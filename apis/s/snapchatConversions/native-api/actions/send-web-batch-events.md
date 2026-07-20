# Send Web Batch Events with Snapchat Conversions

Creates a batch of web conversion events in Snapchat Conversions.

## Endpoint

- **Method:** `POST`
- **Path:** `https://tr.snapchat.com/v3/:pixel_id/events`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Send Web Batch Events](https://developers.snap.com/api/marketing-api/Conversions-API/UsingTheAPI)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pixel_id` | path | `string` | yes | Snapchat Pixel ID that owns the web events. |
| `data` | body | `list<object>` | yes | Array of web conversion events to send in one request. |
| `data[].event_name` | body | `string` | yes | Snap standard or custom event name for the web event. |
| `data[].event_time` | body | `number` | yes | Epoch timestamp in seconds or milliseconds for when the event happened. |
| `data[].event_source_url` | body | `string` | yes | Web page URL where the event took place. |
| `data[].user_data` | body | `object` | no | User matching fields for the event. |
| `data[].user_data.client_ip_address` | body | `string` | no | Device IP address for matching. Do not hash. |
| `data[].user_data.client_user_agent` | body | `string` | no | Device user agent string. Recommended for web events. |
| `data[].user_data.em` | body | `list<string>` | no | Normalized SHA-256 email hashes for user matching. |
| `data[].event_id` | body | `string` | no | Unique event identifier used for deduplication. |
