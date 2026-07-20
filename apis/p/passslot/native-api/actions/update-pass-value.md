# Update Pass Value with Passslot

## Endpoint

- **Method:** `PUT`
- **Path:** `passes/:passTypeIdentifier/:serialNumber/value/:placeholderName`
- **Base URL:** `https://api.passslot.com/v1`
- **Official documentation:** [Update Pass Value](https://www.passslot.com/developer/api/resources/updatePassValue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `passTypeIdentifier` | path | `string` | yes | Passslot pass type identifier. |
| `serialNumber` | path | `string` | yes | Pass serial number. |
| `placeholderName` | path | `string` | yes | Template placeholder name to update on the pass. |
