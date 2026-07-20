# Delete Pass Price with Passslot

## Endpoint

- **Method:** `DELETE`
- **Path:** `passes/:passTypeIdentifier/:serialNumber/price`
- **Base URL:** `https://api.passslot.com/v1`
- **Official documentation:** [Delete Pass Price](https://www.passslot.com/developer/api/resources/deletePassPrice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `passTypeIdentifier` | path | `string` | yes | Passslot pass type identifier. |
| `serialNumber` | path | `string` | yes | Pass serial number. |
