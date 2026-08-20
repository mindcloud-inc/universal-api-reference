# List Tasks with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `tasks`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [List Tasks](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/tasksGET)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[tasks]` | query | `string` | no | Fields: fromCompany, fromProfile, toCompany |
| `fields[companies]` | query | `string` | no | — |
| `fields[properties]` | query | `string` | no | — |
| `fields[productions]` | query | `string` | no | — |
| `include` | query | `string` | no | — |
