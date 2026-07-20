# Get Pass Status with Passslot

## Endpoint

- **Method:** `GET`
- **Path:** `passes/:passTypeIdentifier/:serialNumber/status`
- **Base URL:** `https://api.passslot.com/v1`
- **Official documentation:** [Get Pass Status](https://www.passslot.com/developer/api/resources/showPassStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `passTypeIdentifier` | path | `string` | yes | Passslot pass type identifier. |
| `serialNumber` | path | `string` | yes | Pass serial number. |
