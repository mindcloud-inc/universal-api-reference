# Get Pass Description with Passslot

## Endpoint

- **Method:** `GET`
- **Path:** `passes/:passTypeIdentifier/:serialNumber/passjson`
- **Base URL:** `https://api.passslot.com/v1`
- **Official documentation:** [Get Pass Description](https://www.passslot.com/developer/api/resources/showPassJSON)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `passTypeIdentifier` | path | `string` | yes | Passslot pass type identifier. |
| `serialNumber` | path | `string` | yes | Pass serial number. |
