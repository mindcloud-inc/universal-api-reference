# Create Variant with Swell

## Endpoint

- **Method:** `POST`
- **Path:** `/products\:variants`
- **Base URL:** `https://api.swell.store`
- **Official documentation:** [Create Variant](https://developers.swell.is/backend-api/variants/create-a-variant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent_id` | body | `string` | yes | The parent product ID. |
| `name` | body | `string` | no | The variant name. |
