# Algolia: Native API Reference

A consolidated summary of Algolia's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.algolia.com/doc/rest
- **API base URL:** `https://{applicationId}.algolia.net`

## Authentication

### API Key

Authenticate with Algolia application ID and API key headers.

### Credentials

- **API Key:** `apiKey` · required
- **Application ID:** `applicationId` · required · Your Algolia application ID.

Send these headers with each API request:

```http
x-algolia-api-key: <apiKey>
x-algolia-application-id: <applicationId>
```

[Official authentication documentation](https://www.algolia.com/doc/guides/security/api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `keys`.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add a New Record](actions/add-a-new-record.md) | `POST /1/indexes/:indexName` | [docs](https://www.algolia.com/doc/rest-api/search/save-object) |
| [Add or Replace a Record](actions/add-or-replace-a-record.md) | `PUT /1/indexes/:indexName/:objectID` | [docs](https://www.algolia.com/doc/rest-api/search/add-or-update-object) |
| [Add or Update Attributes](actions/add-or-update-attributes.md) | `POST /1/indexes/:indexName/:objectID/partial` | [docs](https://www.algolia.com/doc/rest-api/search/partial-update-object) |
| [Batch Indexing Operations on Multiple Indices](actions/batch-indexing-operations-on-multiple-indices.md) | `POST /1/indexes/*/batch` | [docs](https://www.algolia.com/doc/rest-api/search/multiple-batch) |
| [Batch Indexing Operations on One Index](actions/batch-indexing-operations-on-one-index.md) | `POST /1/indexes/:indexName/batch` | [docs](https://www.algolia.com/doc/rest-api/search/batch) |
| [Browse for Records](actions/browse-for-records.md) | `POST /1/indexes/:indexName/browse` | [docs](https://www.algolia.com/doc/rest-api/search/browse) |
| [Check Application Task Status](actions/check-application-task-status.md) | `GET /1/task/:taskID` | [docs](https://www.algolia.com/doc/rest-api/search/get-app-task) |
| [Check Task Status](actions/check-task-status.md) | `GET /1/indexes/:indexName/task/:taskID` | [docs](https://www.algolia.com/doc/rest-api/search/get-task) |
| [Copy or Move an Index](actions/copy-or-move-an-index.md) | `POST /1/indexes/:indexName/operation` | [docs](https://www.algolia.com/doc/rest-api/search/operation-index) |
| [Create an API Key](actions/create-an-api-key.md) | `POST /1/keys` | [docs](https://www.algolia.com/doc/rest-api/search/add-api-key) |
| [Create or Replace a Rule](actions/create-or-replace-a-rule.md) | `PUT /1/indexes/:indexName/rules/:objectID` | [docs](https://www.algolia.com/doc/rest-api/search/save-rule) |
| [Create or Replace a Synonym](actions/create-or-replace-a-synonym.md) | `PUT /1/indexes/:indexName/synonyms/:objectID` | [docs](https://www.algolia.com/doc/rest-api/search/save-synonym) |
| [Create or Replace Synonyms](actions/create-or-replace-synonyms.md) | `POST /1/indexes/:indexName/synonyms/batch` | [docs](https://www.algolia.com/doc/rest-api/search/save-synonyms) |
| [Create or Update Rules](actions/create-or-update-rules.md) | `POST /1/indexes/:indexName/rules/batch` | [docs](https://www.algolia.com/doc/rest-api/search/save-rules) |
| [Delete a Record](actions/delete-a-record.md) | `DELETE /1/indexes/:indexName/:objectID` | [docs](https://www.algolia.com/doc/rest-api/search/delete-object) |
| [Delete a Rule](actions/delete-a-rule.md) | `DELETE /1/indexes/:indexName/rules/:objectID` | [docs](https://www.algolia.com/doc/rest-api/search/delete-rule) |
| [Delete a Synonym](actions/delete-a-synonym.md) | `DELETE /1/indexes/:indexName/synonyms/:objectID` | [docs](https://www.algolia.com/doc/rest-api/search/delete-synonym) |
| [Delete All Records from an Index](actions/delete-all-records-from-an-index.md) | `POST /1/indexes/:indexName/clear` | [docs](https://www.algolia.com/doc/rest-api/search/clear-objects) |
| [Delete All Rules](actions/delete-all-rules.md) | `POST /1/indexes/:indexName/rules/clear` | [docs](https://www.algolia.com/doc/rest-api/search/clear-rules) |
| [Delete All Synonyms](actions/delete-all-synonyms.md) | `POST /1/indexes/:indexName/synonyms/clear` | [docs](https://www.algolia.com/doc/rest-api/search/clear-synonyms) |
| [Delete an API Key](actions/delete-an-api-key.md) | `DELETE /1/keys/:key` | [docs](https://www.algolia.com/doc/rest-api/search/delete-api-key) |
| [Delete an Index](actions/delete-an-index.md) | `DELETE /1/indexes/:indexName` | [docs](https://www.algolia.com/doc/rest-api/search/delete-index) |
| [Delete Records Matching a Filter](actions/delete-records-matching-a-filter.md) | `POST /1/indexes/:indexName/deleteByQuery` | [docs](https://www.algolia.com/doc/rest-api/search/delete-by) |
| [List API keys](actions/list-api-keys.md) | `GET /1/keys` | [docs](https://www.algolia.com/doc/rest-api/search/list-api-keys) |
| [List Indices](actions/list-indices.md) | `GET /1/indexes` | [docs](https://www.algolia.com/doc/rest-api/search/list-indices) |
| [Restore an API Key](actions/restore-an-api-key.md) | `POST /1/keys/:key/restore` | [docs](https://www.algolia.com/doc/rest-api/search/restore-api-key) |
| [Retrieve a Record](actions/retrieve-a-record.md) | `GET /1/indexes/:indexName/:objectID` | [docs](https://www.algolia.com/doc/rest-api/search/get-object) |
| [Retrieve a Rule](actions/retrieve-a-rule.md) | `GET /1/indexes/:indexName/rules/:objectID` | [docs](https://www.algolia.com/doc/rest-api/search/get-rule) |
| [Retrieve a Synonym](actions/retrieve-a-synonym.md) | `GET /1/indexes/:indexName/synonyms/:objectID` | [docs](https://www.algolia.com/doc/rest-api/search/get-synonym) |
| [Retrieve API Key Permissions](actions/retrieve-api-key-permissions.md) | `GET /1/keys/:key` | [docs](https://www.algolia.com/doc/rest-api/search/get-api-key) |
| [Retrieve Index Settings](actions/retrieve-index-settings.md) | `GET /1/indexes/:indexName/settings` | [docs](https://www.algolia.com/doc/rest-api/search/get-settings) |
| [Retrieve Log Entries](actions/retrieve-log-entries.md) | `GET /1/logs` | [docs](https://www.algolia.com/doc/rest-api/search/get-logs) |
| [Retrieve Records](actions/retrieve-records.md) | `POST /1/indexes/*/objects` | [docs](https://www.algolia.com/doc/rest-api/search/get-objects) |
| [Search an Index](actions/search-an-index.md) | `POST /1/indexes/:indexName/query` | [docs](https://www.algolia.com/doc/rest-api/search/search-single-index) |
| [Search for Facet Values](actions/search-for-facet-values.md) | `POST /1/indexes/:indexName/facets/:facetName/query` | [docs](https://www.algolia.com/doc/rest-api/search/search-for-facet-values) |
| [Search for Rules](actions/search-for-rules.md) | `POST /1/indexes/:indexName/rules/search` | [docs](https://www.algolia.com/doc/rest-api/search/search-rules) |
| [Search for Synonyms](actions/search-for-synonyms.md) | `POST /1/indexes/:indexName/synonyms/search` | [docs](https://www.algolia.com/doc/rest-api/search/search-synonyms) |
| [Search Multiple Indices](actions/search-multiple-indices.md) | `POST /1/indexes/*/queries` | [docs](https://www.algolia.com/doc/rest-api/search/search) |
| [Update an API Key](actions/update-an-api-key.md) | `PUT /1/keys/:key` | [docs](https://www.algolia.com/doc/rest-api/search/update-api-key) |
| [Update Index Settings](actions/update-index-settings.md) | `PUT /1/indexes/:indexName/settings` | [docs](https://www.algolia.com/doc/rest-api/search/set-settings) |
