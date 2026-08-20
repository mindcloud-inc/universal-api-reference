# List Work Time Entries with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `work_time_entries`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [List Work Time Entries](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/work_time_entriesGET)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[workTimeEntries]` | query | `string` | no | Feilds: lunchBreakMinutes,inAt,outAt     On-Demand Fields: active_hours |
| `fields[profiles]` | query | `string` | no | — |
| `fields[employees]` | query | `string` | no | — |
| `fields[productions]` | query | `string` | no | — |
| `include` | query | `string` | no | — |
