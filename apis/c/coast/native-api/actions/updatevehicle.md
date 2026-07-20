# Update Vehicle By ID with Coast

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/vehicles/:vehicleId`
- **Base URL:** `https://public.coastpay.com`
- **Official documentation:** [Update Vehicle By ID](https://coastpay.com/integrations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vehicleId` | path | `string` | yes | Coast vehicle ID of the vehicle to update. |
| `name` | body | `string` | no | Updated name for the vehicle. |
| `active` | body | `boolean` | no | Whether the vehicle is active in Coast. |
| `licensePlate` | body | `string` | no | Updated license plate for the vehicle. |
| `licensePlateState` | body | `string` | no | Updated license-plate state for the vehicle. |
| `make` | body | `string` | no | Updated make for the vehicle. |
| `model` | body | `string` | no | Updated model for the vehicle. |
| `modelYear` | body | `string` | no | Updated model year for the vehicle. |
| `vin` | body | `string` | no | Updated vehicle identification number. |
| `fuelType` | body | `string` | no | Updated fuel type for the vehicle. |
| `tankCapacity` | body | `string` | no | Updated tank capacity in hundredths of US gallons. |
| `departmentId` | body | `string` | no | Coast department ID to assign to the vehicle. |
| `locationId` | body | `string` | no | Coast location ID to assign to the vehicle. |
| `policyId` | body | `string` | no | Coast policy ID to assign to the vehicle. |
