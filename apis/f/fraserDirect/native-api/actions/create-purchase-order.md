# Create purchase order with Fraser Direct

## Endpoint

- **Method:** `POST`
- **Path:** `/CreatePO`
- **Base URL:** `{baseURL}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PODate` | body | `string` | yes | Required purchase order date in YYYY-MM-DD format. |
| `VendorNumber` | body | `string` | yes | Required vendor number validated against Fraser Direct ERP. |
| `DepositorOrderNumber` | body | `string` | no | DepositorOrderNumber or ShipmentIdentificationNumber must be provided. |
| `ShipmentIdentificationNumber` | body | `string` | no | DepositorOrderNumber or ShipmentIdentificationNumber must be provided. |
| `Priority` | body | `list` | no | Optional priority. Valid values are RUSH or empty. Accepted values: `0`, `1`. |
| `DetailList[]` | body | `array<object>` | yes | Required array of purchase-order line objects. Each line should include LineNumber, QuantityShipped, optional UOM, required SKU, and optional VendorLineNumber. |
