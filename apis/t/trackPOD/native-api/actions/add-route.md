# Add Route with Track-POD

Creates a new route in Track-POD.

## Endpoint

- **Method:** `POST`
- **Path:** `/Route`
- **Base URL:** `https://api.track-pod.com`
- **Official documentation:** [Add Route](https://api.track-pod.com/index.html#/Route/AddRoute)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Code` | body | `string` | no | Route code. |
| `Date` | body | `string` | no | Route date and time. |
| `Depot` | body | `string` | no | Depot name. |
| `DepotId` | body | `string` | no | Depot identifier. |
| `DriverLogin` | body | `string` | no | Driver login. |
| `DriverName` | body | `string` | no | Driver name. |
| `DriverPassword` | body | `string` | no | Driver password. |
| `DriverVehicle` | body | `string` | no | Driver vehicle. |
| `Id` | body | `string` | no | Route identifier. |
| `Orders[0].Address` | body | `string` | no | First route order address. |
| `Orders[0].ContactName` | body | `string` | no | First route order contact name. |
| `Orders[0].Date` | body | `string` | no | First route order date and time. |
| `Orders[0].Note` | body | `string` | no | First route order note. |
| `Orders[0].Number` | body | `string` | no | First route order number. |
| `Orders[0].Phone` | body | `string` | no | First route order phone. |
| `Orders[0].TimeSlotFrom` | body | `string` | no | First route order time window start. |
| `Orders[0].TimeSlotTo` | body | `string` | no | First route order time window end. |
| `Orders[1].Address` | body | `string` | no | Second route order address. |
| `Orders[1].ContactName` | body | `string` | no | Second route order contact name. |
| `Orders[1].Date` | body | `string` | no | Second route order date and time. |
| `Orders[1].Note` | body | `string` | no | Second route order note. |
| `Orders[1].Number` | body | `string` | no | Second route order number. |
| `Orders[1].Phone` | body | `string` | no | Second route order phone. |
| `Orders[1].TimeSlotFrom` | body | `string` | no | Second route order time window start. |
| `Orders[1].TimeSlotTo` | body | `string` | no | Second route order time window end. |
| `ReturnToDepot` | body | `boolean` | no | Whether the route returns to the depot. |
| `RouteDate` | body | `string` | no | Route date and time. |
| `StartFromDepot` | body | `boolean` | no | Whether the route starts from the depot. |
| `StartTimePlan` | body | `string` | no | Planned route start time. |
| `Vehicle.Carrier` | body | `string` | no | Route vehicle carrier. |
| `Vehicle.CarrierCode` | body | `string` | no | Route vehicle carrier code. |
| `Vehicle.Number` | body | `string` | no | Route vehicle number. |
| `Vehicle.Pallets` | body | `number` | no | Route vehicle pallet capacity. |
| `Vehicle.Volume` | body | `number` | no | Route vehicle volume capacity. |
| `Vehicle.Weight` | body | `number` | no | Route vehicle weight capacity. |
