# Update Variant with Swell

## Endpoint

- **Method:** `PUT`
- **Path:** `/products\:variants/:id`
- **Base URL:** `https://api.swell.store`
- **Official documentation:** [Update Variant](https://developers.swell.is/backend-api/variants/update-a-variant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Swell variant ID. |
| `parent_id` | body | `string` | yes | The parent product ID. |
| `name` | body | `string` | no | The variant name. |
