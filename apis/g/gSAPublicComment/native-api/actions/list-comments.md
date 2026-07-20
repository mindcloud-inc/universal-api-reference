# List Comments with GSA Public Comment

Retrieves a list of comments from GSA Public Comment.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments`
- **Base URL:** `https://api.regulations.gov/v4`
- **Official documentation:** [List Comments](https://open.gsa.gov/api/regulationsgov/#searching-for-comments)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[agencyId]` | query | `string` | no | Filter comments by agency acronym, such as EPA. |
| `filter[searchTerm]` | query | `string` | no | Filter comments by keyword or identifier. |
| `filter[commentOnId]` | query | `string` | no | Filter comments by the objectId of the document being commented on. |
| `filter[postedDate]` | query | `date` | no | Filter comments by posted date in yyyy-MM-dd format. |
| `filter[lastModifiedDate]` | query | `date` | no | Filter comments by last modified date in yyyy-MM-dd HH:mm:ss format. |
