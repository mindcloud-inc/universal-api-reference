# Add Driver with Track-POD

Creates a new driver in Track-POD.

## Endpoint

- **Method:** `POST`
- **Path:** `/Driver`
- **Base URL:** `https://api.track-pod.com`
- **Official documentation:** [Add Driver](https://api.track-pod.com/index.html#/Driver/AddDriver)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Active` | body | `boolean` | no | Whether the driver is active. |
| `Depot` | body | `string` | no | Depot name. |
| `DepotId` | body | `string` | no | Depot identifier. |
| `HomeAddress` | body | `string` | no | Driver home address. |
| `Name` | body | `string` | no | Driver name. |
| `Note` | body | `string` | no | Driver note. |
| `Password` | body | `string` | no | Driver password for Track-POD. |
| `Phone` | body | `string` | no | Driver phone number. |
| `Username` | body | `string` | no | Driver username for Track-POD. |
| `Vehicle` | body | `string` | no | Assigned vehicle number or name. |
| `Zone` | body | `string` | no | Driver zone. |
