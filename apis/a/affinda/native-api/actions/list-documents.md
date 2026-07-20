# Get list of all documents with Affinda

Retrieves accessible document summaries from Affinda.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/documents`
- **Base URL:** `https://api.us1.affinda.com`
- **Official documentation:** [Get list of all documents](https://docs.affinda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | query | `string` | no | Filter by collection. |
| `compact` | query | `string` | no | If "true", the response is compacted to annotations' parsed data. Annotations' meta data are excluded. Default is "false". |
| `count` | query | `string` | no | If "false", the documents count is not computed, thus saving time for large collections. Default is "true". |
| `created_dt` | query | `string` | no | Filter by created datetime. |
| `custom_identifier` | query | `string` | no | Filter for documents with this custom identifier. |
| `exclude` | query | `string` | no | Exclude some documents from the result. |
| `failed` | query | `string` | no | Filter by failed status. |
| `has_challenges` | query | `string` | no | Filter for documents with challenges. |
| `in_review` | query | `string` | no | Exclude documents that are currently being reviewed. |
| `include_data` | query | `string` | no | By default, this endpoint returns only the meta data of the documents. Set this to `true` will return a summary of the data that was parsed. If you want to retrieve the full set of data for a document, use the `GET /documents/{identifier}` endpoint. |
| `limit` | query | `string` | no | The numbers of results to return. |
| `offset` | query | `string` | no | The number of documents to skip before starting to collect the result set. |
| `ordering` | query | `string` | no | Sort the result set. A "-" at the beginning denotes DESC sort, e.g. -created_dt. Sort by multiple fields is supported. Supported values include: 'file_name', 'extractor', 'created_dt', 'validated_dt', 'archived_dt' and 'parsed__<dataPointSlug>'. |
| `ready` | query | `string` | no | Filter by ready status. |
| `search` | query | `string` | no | Partial, case-insensitive match with file name or tag name. |
| `snake_case` | query | `string` | no | Whether to return the response in snake_case instead of camelCase. Default is false. |
| `state` | query | `string` | no | Filter by the document's state. |
| `tags` | query | `string` | no | Filter by tag's IDs. |
| `validatable` | query | `string` | no | Filter for validatable documents. |
| `workspace` | query | `string` | no | Filter by workspace. |
