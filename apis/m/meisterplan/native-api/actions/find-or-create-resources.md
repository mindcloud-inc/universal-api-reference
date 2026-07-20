# Find Or Create Resources with Meisterplan

Finds resources in Meisterplan, or creates them if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/resources/findOrCreateResources`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Find Or Create Resources](https://api.us.meisterplan.com/docs/api.html#operation/FindOrCreateResources)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `items[]` | body | `array<object>` | yes |
