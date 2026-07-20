# Create Segment with Simpleen Translation

Creates a new segment in Simpleen Translation.

## Endpoint

- **Method:** `POST`
- **Path:** `/segments`
- **Base URL:** `https://api.simpleen.io`
- **Official documentation:** [Create Segment](https://simpleen.io/documentation/api-reference#post-segments)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `source_entry` | body | `string` | yes |
| `entry` | body | `string` | yes |
| `service` | body | `string` | yes |
| `formality` | body | `string` | yes |
| `interpolation` | body | `string` | yes |
| `source_language` | body | `number` | yes |
| `target_language` | body | `number` | yes |
