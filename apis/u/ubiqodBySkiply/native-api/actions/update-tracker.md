# Update Tracker with Ubiqod by Skiply

## Endpoint

- **Method:** `PATCH`
- **Path:** `/trackers/:trackerSlug`
- **Base URL:** `https://api.ubiqod.com`
- **Official documentation:** [Update Tracker](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trackerSlug` | path | `string` | yes | Tracker slug. |
| `label` | body | `string` | no | Updated tracker label. |
| `site_id` | body | `string` | no | Updated site ID attached to the tracker. |
| `interface_id` | body | `string` | no | Updated interface ID attached to the tracker. |
| `dispatches[]` | body | `array<string>` | no | Updated dispatch IDs attached to the tracker. |
