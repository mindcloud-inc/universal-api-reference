# Create QR Code Tracker with Ubiqod by Skiply

## Endpoint

- **Method:** `POST`
- **Path:** `/trackers/`
- **Base URL:** `https://api.ubiqod.com`
- **Official documentation:** [Create QR Code Tracker](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | body | `string` | yes | Tracker label. |
| `site_id` | body | `string` | no | Site ID to attach to the tracker. |
| `interface_id` | body | `string` | no | Interface ID to attach to the tracker. |
| `dispatches[]` | body | `array<string>` | no | Dispatch IDs attached to the tracker. |
