# Retrieve Variant with Katana

Retrieves a variant by ID from Katana.

## Endpoint

- **Method:** `GET`
- **Path:** `/variants/:id`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Retrieve Variant](https://developer.katanamrp.com/reference/getvariant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Variant id |
| `extend[]` | query | `array<string>` | no | Array of objects that need to be added to the response |
