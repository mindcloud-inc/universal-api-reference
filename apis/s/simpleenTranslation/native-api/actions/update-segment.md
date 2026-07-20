# Update Segment with Simpleen Translation

Updates an existing segment in Simpleen Translation.

## Endpoint

- **Method:** `PUT`
- **Path:** `/segments/:id`
- **Base URL:** `https://api.simpleen.io`
- **Official documentation:** [Update Segment](https://simpleen.io/documentation/api-reference#putdelete-segmentsid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `source_entry` | body | `string` | yes |
| `entry` | body | `string` | yes |
| `service` | body | `string` | yes |
| `formality` | body | `string` | yes |
| `interpolation` | body | `string` | yes |
| `source_language` | body | `number` | yes |
| `target_language` | body | `number` | yes |
