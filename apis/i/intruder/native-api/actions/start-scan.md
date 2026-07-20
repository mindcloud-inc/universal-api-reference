# Start Scan with Intruder

## Endpoint

- **Method:** `POST`
- **Path:** `/scans/`
- **Base URL:** `https://api.intruder.io/v1`
- **Official documentation:** [Start Scan](https://developers.intruder.io/reference/scans_create-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_addresses[]` | body | `array<string>` | no | Optional target addresses to scan. Leave empty to scan all targets. |
| `tag_names[]` | body | `array<string>` | no | Optional target tag names to scan. |
| `throttled` | body | `boolean` | no | Throttle the scan for reduced scan intensity. |
| `web_ports_only` | body | `boolean` | no | Limit the scan to common web ports only. |
