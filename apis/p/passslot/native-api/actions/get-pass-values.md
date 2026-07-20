# Get Pass Values with Passslot

## Endpoint

- **Method:** `GET`
- **Path:** `passes/:passTypeIdentifier/:serialNumber/values`
- **Base URL:** `https://api.passslot.com/v1`
- **Official documentation:** [Get Pass Values](https://www.passslot.com/developer/api/resources/showPassValues)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `passTypeIdentifier` | path | `string` | yes | Passslot pass type identifier. |
| `serialNumber` | path | `string` | yes | Pass serial number. |
