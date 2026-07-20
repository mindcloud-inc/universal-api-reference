# Push Pass with Passslot

## Endpoint

- **Method:** `POST`
- **Path:** `passes/:passTypeIdentifier/:serialNumber/push`
- **Base URL:** `https://api.passslot.com/v1`
- **Official documentation:** [Push Pass](https://www.passslot.com/developer/api/resources/pushPass)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `passTypeIdentifier` | path | `string` | yes | Passslot pass type identifier. |
| `serialNumber` | path | `string` | yes | Pass serial number. |
