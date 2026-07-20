# List Documents with GSA Public Comment

Retrieves a list of documents from GSA Public Comment.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents`
- **Base URL:** `https://api.regulations.gov/v4`
- **Official documentation:** [List Documents](https://open.gsa.gov/api/regulationsgov/#searching-for-documents)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[agencyId]` | query | `string` | no | Filter documents by agency acronym, such as EPA. |
| `filter[searchTerm]` | query | `string` | no | Filter documents by keyword or identifier. |
| `filter[docketId]` | query | `string` | no | Filter documents by docket ID. |
| `filter[documentType]` | query | `string` | no | Filter documents by document type. |
| `filter[frDocNum]` | query | `string` | no | Filter documents by Federal Register document number. |
| `filter[postedDate]` | query | `date` | no | Filter documents by posted date in yyyy-MM-dd format. |
| `filter[commentEndDate]` | query | `date` | no | Filter documents by comment end date in yyyy-MM-dd format. |
| `filter[lastModifiedDate]` | query | `date` | no | Filter documents by last modified date in yyyy-MM-dd HH:mm:ss format. |
| `filter[subtype]` | query | `string` | no | Filter documents by subtype. |
| `filter[withinCommentPeriod]` | query | `boolean` | no | Set to true to return documents open for comment. |
