# Send Pass by Email with Passslot

## Endpoint

- **Method:** `POST`
- **Path:** `passes/:passTypeIdentifier/:serialNumber/email`
- **Base URL:** `https://api.passslot.com/v1`
- **Official documentation:** [Send Pass by Email](https://www.passslot.com/developer/api/resources/sendPassEmail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `passTypeIdentifier` | path | `string` | yes | Passslot pass type identifier. |
| `serialNumber` | path | `string` | yes | Pass serial number. |
