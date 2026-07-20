# Update Pass Status with Passslot

## Endpoint

- **Method:** `PUT`
- **Path:** `passes/:passTypeIdentifier/:serialNumber/status`
- **Base URL:** `https://api.passslot.com/v1`
- **Official documentation:** [Update Pass Status](https://www.passslot.com/developer/api/resources/updatePassStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `passTypeIdentifier` | path | `string` | yes | Passslot pass type identifier. |
| `serialNumber` | path | `string` | yes | Pass serial number. |
