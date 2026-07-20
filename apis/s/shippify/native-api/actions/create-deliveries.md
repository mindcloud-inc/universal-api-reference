# Create Deliveries with Shippify

Creates up to 100 deliveries in Shippify.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/deliveries`
- **Base URL:** `https://api.shippify.co`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | body | `number` | no | Optional Shippify company identifier where the deliveries will be created. |
| `type` | body | `string` | no | Optional Shippify delivery type such as slot, express, or flex. |
| `deliveries[]` | body | `array<object>` | yes | Required array of Shippify delivery payload objects using the documented pickup, dropoff, packages, referenceId, tags, extraData, and cod structure. |
