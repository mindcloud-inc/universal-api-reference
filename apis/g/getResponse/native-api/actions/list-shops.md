# List Shops with GetResponse

Retrieves a list of shops from GetResponse.

## Endpoint

- **Method:** `GET`
- **Path:** `/shops`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [List Shops](https://apireference.getresponse.com/#operation/getShopList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query[name]` | query | `string` | no | Search shops by name |
| `sort[name]` | query | `string` | no | Sort by name |
| `sort[createdOn]` | query | `string` | no | Sort by creation date |
| `fields` | query | `string` | no | Comma-separated list of fields to return |
