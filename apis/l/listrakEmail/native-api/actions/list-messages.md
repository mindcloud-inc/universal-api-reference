# List Messages with Listrak Email

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/List/:listID/Message`
- **Base URL:** `https://api.listrak.com/email`
- **Official documentation:** [List Messages](https://api.listrak.com/email#tag/List)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `startDate` | query | `string` | no |
| `endDate` | query | `string` | no |
| `includeTestMessages` | query | `string` | no |
| `listID` | path | `string` | yes |
