# Change Property Label with Wasi

Updates a property label in Wasi.

## Endpoint

- **Method:** `POST`
- **Path:** `/property/change-label/:id_property`
- **Base URL:** `https://api.wasi.co/v1`
- **Official documentation:** [Change Property Label](https://api.wasi.co/docs/en/guide/properties.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_property` | path | `number` | yes | Wasi property ID. |
| `label` | query | `string` | yes | Property label to set. |
