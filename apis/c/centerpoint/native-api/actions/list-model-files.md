# List Model Files with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `model_files`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [List Model Files](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/model_filesGET)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fields[profiles]` | query | `string` | no |
| `fields[employees]` | query | `string` | no |
| `filter[subjectId]` | query | `number` | no |
| `fields[buildingDivisions]` | query | `string` | no |
| `filter[subjectType]` | query | `string` | no |
| `filter[tag]` | query | `string` | no |
| `include` | query | `string` | no |
| `sort` | query | `string` | no |
