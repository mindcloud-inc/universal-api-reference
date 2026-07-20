# Validate Test Events with Snapchat Conversions

Validates test conversion events in Snapchat Conversions.

## Endpoint

- **Method:** `POST`
- **Path:** `https://tr.snapchat.com/v3/:asset_id/events/validate`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Validate Test Events](https://developers.snap.com/api/marketing-api/Conversions-API/VerifySetUp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asset_id` | path | `string` | yes | Valid Snapchat Pixel ID or Snap App ID associated with the token. |
| `data[]` | body | `array<object>` | yes | Array of test conversion events to validate. |
| `data[].event_name` | body | `string` | yes | Snap conversion event name to validate. |
| `data[].event_time` | body | `number` | yes | Epoch timestamp for the event, within the past seven days. |
| `data[].action_source` | body | `string` | yes | Where the event took place. |
| `data[].event_source_url` | body | `string` | yes | URL where the web event occurred. |
| `data[].user_data` | body | `object` | yes | User matching fields for the event. |
| `data[].user_data.em[]` | body | `array<string>` | yes | SHA-256 normalized email hashes for matching. |
