# List Events with SavvyCal

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/events`
- **Base URL:** `https://api.savvycal.com`
- **Official documentation:** [List Events](https://developers.savvycal.com/api/list-events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `state` | query | `string` | no |
| `period` | query | `string` | no |
| `from` | query | `date` | no |
| `until` | query | `date` | no |
| `direction` | query | `string` | no |
| `attendance` | query | `string` | no |
| `link` | query | `string` | no |
