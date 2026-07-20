# Update Supplier with Katana

Updates an existing supplier in Katana.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/suppliers/:id`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Update Supplier](https://developer.katanamrp.com/reference/updatesupplier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Supplier id |
| `name` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
| `currency` | body | `string` | no | The supplier’s currency (ISO 4217). |
| `comment` | body | `string` | no | — |
