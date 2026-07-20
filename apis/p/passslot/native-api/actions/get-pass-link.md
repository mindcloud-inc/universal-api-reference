# Get Pass Link with Passslot

## Endpoint

- **Method:** `GET`
- **Path:** `passes/:passTypeIdentifier/:serialNumber/url`
- **Base URL:** `https://api.passslot.com/v1`
- **Official documentation:** [Get Pass Link](https://www.passslot.com/developer/api/resources/showPassURL)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `passTypeIdentifier` | path | `string` | yes | Passslot pass type identifier. |
| `serialNumber` | path | `string` | yes | Pass serial number. |
