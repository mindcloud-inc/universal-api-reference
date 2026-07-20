# List Dockets with GSA Public Comment

Retrieves a list of dockets from GSA Public Comment.

## Endpoint

- **Method:** `GET`
- **Path:** `/dockets`
- **Base URL:** `https://api.regulations.gov/v4`
- **Official documentation:** [List Dockets](https://open.gsa.gov/api/regulationsgov/#searching-for-dockets)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[agencyId]` | query | `string` | no | Filter dockets by agency acronym, such as EPA. |
| `filter[searchTerm]` | query | `string` | no | Filter dockets by keyword or identifier. |
| `filter[docketType]` | query | `string` | no | Filter dockets by docket type. |
| `filter[lastModifiedDate]` | query | `date` | no | Filter dockets by last modified date in yyyy-MM-dd HH:mm:ss format. |
