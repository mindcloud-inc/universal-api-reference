# List Employees with Housecall Pro

## Endpoint

- **Method:** `GET`
- **Path:** `/employees`
- **Base URL:** `https://api.housecallpro.com`
- **Official documentation:** [List Employees](https://docs.housecallpro.com/docs/housecall-public-api/303ee235f23fa-get-employees)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location_ids[]` | query | `array<string>` | no | IDs of locations to pull employees from. Send multiple values as a array. |
