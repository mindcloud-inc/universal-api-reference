# Create Vehicle with Coast

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/vehicles`
- **Base URL:** `https://public.coastpay.com`
- **Official documentation:** [Create Vehicle](https://coastpay.com/integrations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Friendly name for the vehicle. |
| `active` | body | `boolean` | yes | Whether the vehicle is active in Coast. |
| `licensePlate` | body | `string` | no | License plate for the vehicle. |
| `licensePlateState` | body | `string` | no | State associated with the vehicle license plate. |
| `make` | body | `string` | no | Vehicle make. |
| `model` | body | `string` | no | Vehicle model. |
| `modelYear` | body | `string` | no | Vehicle model year. |
| `vin` | body | `string` | no | Vehicle identification number. |
| `fuelType` | body | `string` | no | Vehicle fuel type. |
| `tankCapacity` | body | `string` | no | Tank capacity in hundredths of US gallons. |
| `departmentId` | body | `string` | no | Coast department ID to assign to the vehicle. |
| `locationId` | body | `string` | no | Coast location ID to assign to the vehicle. |
| `policyId` | body | `string` | no | Coast policy ID to assign to the vehicle. |
