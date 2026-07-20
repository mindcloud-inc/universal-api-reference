# Retrieve Design By ID with Zakeke

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/designs/{designID}/{quantity}`
- **Base URL:** `https://api.zakeke.com`
- **Official documentation:** [Retrieve Design By ID](https://docs.zakeke.com/docs/API/designs-API#4-retrieve-a-design-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `designID` | path | `string` | yes | Unique design identifier provided by Zakeke. |
| `quantity` | path | `number` | yes | Quantity used to calculate design pricing and totals. |
| `modificationID` | query | `string` | no | Optional identifier for a specific names-and-numbers or bulk-variation instance. |
