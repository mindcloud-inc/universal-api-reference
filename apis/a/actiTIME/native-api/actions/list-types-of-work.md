# List Types of Work with actiTIME

Retrieves a list of types of work from actiTIME.

## Endpoint

- **Method:** `GET`
- **Path:** `/typesOfWork`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [List Types of Work](https://www.actitime.com/api-documentation/types-of-work-resource)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `boolean` | no | Filter archived vs active types of work. |
| `billable` | query | `boolean` | no | Filter billable vs non-billable types of work. |
| `ids` | query | `string` | no | Comma-separated type of work ids to return. |
| `name` | query | `string` | no | Exact type of work name match, case-insensitive. |
| `sort` | query | `string` | no | Sorting tokens like +name or -name. |
| `words` | query | `string` | no | Return types of work containing all given words in the name. |
