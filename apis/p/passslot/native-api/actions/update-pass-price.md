# Update Pass Price with Passslot

## Endpoint

- **Method:** `PUT`
- **Path:** `passes/:passTypeIdentifier/:serialNumber/price`
- **Base URL:** `https://api.passslot.com/v1`
- **Official documentation:** [Update Pass Price](https://www.passslot.com/developer/api/resources/updatePassPrice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `passTypeIdentifier` | path | `string` | yes | Passslot pass type identifier. |
| `serialNumber` | path | `string` | yes | Pass serial number. |
