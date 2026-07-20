# Retrieve Composition By ID with Zakeke

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/compositions/{compositionID}/{quantity}`
- **Base URL:** `https://api.zakeke.com`
- **Official documentation:** [Retrieve Composition By ID](https://docs.zakeke.com/docs/API/compositions-API#4-retrieve-a-composition-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `compositionID` | path | `string` | yes | Unique configuration identifier provided by Zakeke. |
| `quantity` | path | `number` | yes | Quantity used to calculate composition pricing and totals. |
