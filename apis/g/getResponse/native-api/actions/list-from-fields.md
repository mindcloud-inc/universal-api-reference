# List From Fields with GetResponse

Retrieves From addresses from GetResponse.

## Endpoint

- **Method:** `GET`
- **Path:** `/from-fields`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [List From Fields](https://apireference.getresponse.com/#operation/getFromFieldList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query[email]` | query | `string` | no | Filter from fields by email |
| `query[name]` | query | `string` | no | Filter from fields by name |
| `query[isDefault]` | query | `string` | no | Filter by default sender flag |
| `query[isActive]` | query | `string` | no | Filter by active sender flag |
| `fields` | query | `string` | no | Comma-separated list of fields to return |
