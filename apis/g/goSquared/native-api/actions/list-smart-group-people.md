# List Smart Group People with GoSquared

Retrieves people from a GoSquared smart group.

## Endpoint

- **Method:** `GET`
- **Path:** `people/v1/smartgroups/:groupID/people`
- **Base URL:** `https://api.gosquared.com`
- **Official documentation:** [List Smart Group People](https://www.gosquared.com/docs/people/smartgroups/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupID` | path | `string` | yes | The identifier of the Smart Group whose People should be listed. |
| `query` | query | `string` | no | The query term used to search within the Smart Group. |
| `fields` | query | `string` | no | A comma-delimited list of fields to include in each result row. |
| `presenter` | query | `string` | no | Modifies the response data structure. |
| `dateFormat` | query | `string` | no | Moment-compatible format for returned date values. |
