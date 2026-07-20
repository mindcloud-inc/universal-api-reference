# Update Vehicle with Track-POD

Updates an existing vehicle in Track-POD.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Vehicle`
- **Base URL:** `https://api.track-pod.com`
- **Official documentation:** [Update Vehicle](https://api.track-pod.com/index.html#/Vehicle/UpdateVehicle)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BaseFare` | body | `number` | no | Base fare. |
| `Carrier` | body | `string` | no | Carrier name. |
| `CarrierCode` | body | `string` | no | Carrier code. |
| `CostPerDistance` | body | `number` | no | Cost per distance unit. |
| `CostPerHour` | body | `number` | no | Cost per hour. |
| `Depot` | body | `string` | no | Depot name. |
| `DepotId` | body | `string` | no | Depot identifier. |
| `DriverId` | body | `string` | no | Assigned driver identifier. |
| `DriverUsername` | body | `string` | no | Assigned driver username. |
| `EmissionCo2` | body | `number` | no | CO2 emission value. |
| `Id` | body | `string` | no | Track-POD unique identifier for the vehicle. |
| `MaxDistance` | body | `number` | no | Maximum travel distance. |
| `MaxNodes` | body | `number` | no | Maximum route nodes. |
| `MaxWorkTime` | body | `number` | no | Maximum work time. |
| `Number` | body | `string` | no | Vehicle number. |
| `Pallets` | body | `number` | no | Vehicle pallet capacity. |
| `SpeedRatio` | body | `number` | no | Speed ratio. |
| `StartTime` | body | `string` | no | Vehicle start time. |
| `VehicleType` | body | `string` | no | Vehicle type identifier. |
| `Volume` | body | `number` | no | Vehicle volume capacity. |
| `Weight` | body | `number` | no | Vehicle weight capacity. |
