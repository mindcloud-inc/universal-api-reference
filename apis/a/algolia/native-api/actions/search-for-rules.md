# Search for Rules with Algolia

Searches for rules in an Algolia index.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/indexes/:indexName/rules/search`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Search for Rules](https://www.algolia.com/doc/rest-api/search/search-rules)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | Name of the index on which to search rules. |
| `query` | body | `string` | no | Text query to match rule object IDs or descriptions. |
| `anchoring` | body | `string` | no | Anchoring strategy for rule conditions. |
| `context` | body | `string` | no | Rule context to filter by. |
| `page` | body | `number` | no | Results page number. |
| `hitsPerPage` | body | `number` | no | Maximum number of rules to return. |
| `enabled` | body | `boolean` | no | Whether to return only enabled or disabled rules. |
