# Add devices to blocklist with Veryfi

Adds devices to Veryfi's blocklist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v8/partner/fraud/blocklist`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Add devices to blocklist](https://docs.veryfi.com/api/add-devices-to-blocklist/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device_ids[]` | body | `array<object>` | yes | Possible values: >= 1 string string |
