# List Driver-Vehicle Assignments with Samsara

## Endpoint

- **Method:** `GET`
- **Path:** `fleet/driver-vehicle-assignments`
- **Base URL:** `https://api.samsara.com/`
- **Official documentation:** [List Driver-Vehicle Assignments](https://developers.samsara.com/reference/getdrivervehicleassignments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filterBy` | query | `string` | yes | Whether to filter assignments by drivers or vehicles. |
| `startTime` | query | `string` | no | Assignment range start in RFC 3339 format. |
| `endTime` | query | `string` | no | Assignment range end in RFC 3339 format. |
