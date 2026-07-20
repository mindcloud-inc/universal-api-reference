# List Custom Fields with GetResponse

Retrieves a list of custom fields from GetResponse.

## Endpoint

- **Method:** `GET`
- **Path:** `/custom-fields`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [List Custom Fields](https://apireference.getresponse.com/#operation/getCustomFieldList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query[name]` | query | `string` | no | Filter custom fields by name |
| `sort[name]` | query | `string` | no | Sort custom fields by name |
| `fields` | query | `string` | no | Comma-separated list of fields to return |
