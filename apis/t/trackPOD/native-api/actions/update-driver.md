# Update Driver with Track-POD

Updates an existing driver in Track-POD.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Driver`
- **Base URL:** `https://api.track-pod.com`
- **Official documentation:** [Update Driver](https://api.track-pod.com/index.html#/Driver/UpdateDriver)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Active` | body | `boolean` | no | Whether the driver is active. |
| `Depot` | body | `string` | no | Depot name. |
| `DepotId` | body | `string` | no | Depot identifier. |
| `HomeAddress` | body | `string` | no | Driver home address. |
| `Id` | body | `string` | no | Track-POD unique identifier for the driver. |
| `Name` | body | `string` | no | Driver name. |
| `Note` | body | `string` | no | Driver note. |
| `Password` | body | `string` | no | Driver password for Track-POD. |
| `Phone` | body | `string` | no | Driver phone number. |
| `Username` | body | `string` | no | Driver username for Track-POD. |
| `Vehicle` | body | `string` | no | Assigned vehicle number or name. |
| `Zone` | body | `string` | no | Driver zone. |
