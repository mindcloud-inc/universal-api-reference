# Get purchase order information with Fraser Direct

## Endpoint

- **Method:** `GET`
- **Path:** `/GetPOInformation`
- **Base URL:** `{baseURL}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `DepositorOrderNumber` | body | `string` | no | Provide DepositorOrderNumber, ShipmentIdentificationNumber, or both. |
| `ShipmentIdentificationNumber` | body | `string` | no | Provide DepositorOrderNumber, ShipmentIdentificationNumber, or both. If both are provided, they must match the same purchase order. |
