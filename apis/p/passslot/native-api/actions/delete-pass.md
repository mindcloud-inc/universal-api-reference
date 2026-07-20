# Delete Pass with Passslot

## Endpoint

- **Method:** `DELETE`
- **Path:** `passes/:passTypeIdentifier/:serialNumber`
- **Base URL:** `https://api.passslot.com/v1`
- **Official documentation:** [Delete Pass](https://www.passslot.com/developer/api/resources/deletePass)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `passTypeIdentifier` | path | `string` | yes | Passslot pass type identifier. |
| `serialNumber` | path | `string` | yes | Pass serial number. |
