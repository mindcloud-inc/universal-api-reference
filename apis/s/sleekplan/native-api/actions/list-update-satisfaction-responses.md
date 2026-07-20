# List Update Satisfaction Responses with Sleekplan

## Endpoint

- **Method:** `GET`
- **Path:** `/update/:updateid/satisfaction`
- **Base URL:** `https://api.sleekplan.com/v1`
- **Official documentation:** [List Update Satisfaction Responses](https://sleekplan.com/docs/api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `date_end` | query | `date` | no |
| `date_start` | query | `date` | no |
| `segment` | query | `string` | no |
| `updateid` | path | `string` | yes |
