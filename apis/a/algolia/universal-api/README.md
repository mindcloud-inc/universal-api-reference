# <img src="https://images.mindcloud.co/apps/icons/algolia_1776096766566.png" alt="Algolia logo" width="28" height="28"> Algolia: Universal API

Manage Algolia indices, records, search settings, and API keys.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/algolia/latest
- **Category:** IT Operations / Database
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.algolia.com
- **Vendor API docs:** https://www.algolia.com/doc/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List API keys](actions/list-api-keys.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/list-api-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Create an API Key](actions/create-an-api-key.md) | POST | Creates a new API key in Algolia. |
| [Delete an API Key](actions/delete-an-api-key.md) | DELETE | Deletes an API key from Algolia. |
| [List API keys](actions/list-api-keys.md) | GET | Retrieves all API keys from Algolia. |
| [Restore an API Key](actions/restore-an-api-key.md) | POST | Restores a deleted API key in Algolia. |
| [Retrieve API Key Permissions](actions/retrieve-api-key-permissions.md) | GET | Retrieves API key permissions and restrictions from Algolia. |
| [Update an API Key](actions/update-an-api-key.md) | PUT | Updates an existing API key in Algolia. |

### Facet Value

| Action | Method | Description |
| --- | --- | --- |
| [Search for Facet Values](actions/search-for-facet-values.md) | GET | Searches facet values in an Algolia index. |

### Index

| Action | Method | Description |
| --- | --- | --- |
| [Copy or Move an Index](actions/copy-or-move-an-index.md) | PUT | Copies or moves an Algolia index. |
| [Delete an Index](actions/delete-an-index.md) | DELETE | Deletes an existing index from Algolia. |
| [List Indices](actions/list-indices.md) | GET | Retrieves all indices in the Algolia application. |
| [Retrieve Index Settings](actions/retrieve-index-settings.md) | GET | Retrieves all index settings from Algolia. |
| [Update Index Settings](actions/update-index-settings.md) | PUT | Updates existing index settings in Algolia. |

### Log Entry

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Log Entries](actions/retrieve-log-entries.md) | GET | Retrieves log entries from the Algolia application. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Add a New Record](actions/add-a-new-record.md) | POST | Creates a new record in an Algolia index. |
| [Add or Replace a Record](actions/add-or-replace-a-record.md) | PUT | Adds or replaces a record in Algolia. |
| [Add or Update Attributes](actions/add-or-update-attributes.md) | PUT | Adds or updates record attributes in Algolia. |
| [Batch Indexing Operations on Multiple Indices](actions/batch-indexing-operations-on-multiple-indices.md) | POST | Runs batch indexing operations on multiple Algolia indices. |
| [Batch Indexing Operations on One Index](actions/batch-indexing-operations-on-one-index.md) | POST | Runs batch indexing operations on one Algolia index. |
| [Browse for Records](actions/browse-for-records.md) | GET | Browses records in an Algolia index. |
| [Delete a Record](actions/delete-a-record.md) | DELETE | Deletes a record from an Algolia index. |
| [Delete All Records from an Index](actions/delete-all-records-from-an-index.md) | DELETE | Deletes all records from an Algolia index. |
| [Delete Records Matching a Filter](actions/delete-records-matching-a-filter.md) | DELETE | Deletes records matching a filter in Algolia. |
| [Retrieve a Record](actions/retrieve-a-record.md) | GET | Retrieves a record from an Algolia index. |
| [Retrieve Records](actions/retrieve-records.md) | GET | Retrieves records from one or more Algolia indices. |
| [Search an Index](actions/search-an-index.md) | GET | Searches one Algolia index for matching records. |
| [Search Multiple Indices](actions/search-multiple-indices.md) | GET | Searches multiple Algolia indices in one request. |

### Rule

| Action | Method | Description |
| --- | --- | --- |
| [Create or Replace a Rule](actions/create-or-replace-a-rule.md) | POST | Creates or replaces a rule in Algolia. |
| [Create or Update Rules](actions/create-or-update-rules.md) | POST | Creates or updates multiple rules in Algolia. |
| [Delete a Rule](actions/delete-a-rule.md) | DELETE | Deletes an existing rule from Algolia. |
| [Delete All Rules](actions/delete-all-rules.md) | DELETE | Deletes all rules from an Algolia index. |
| [Retrieve a Rule](actions/retrieve-a-rule.md) | GET | Retrieves an existing rule from Algolia. |
| [Search for Rules](actions/search-for-rules.md) | GET | Searches for rules in an Algolia index. |

### Synonym

| Action | Method | Description |
| --- | --- | --- |
| [Create or Replace a Synonym](actions/create-or-replace-a-synonym.md) | POST | Creates or replaces a synonym in Algolia. |
| [Create or Replace Synonyms](actions/create-or-replace-synonyms.md) | POST | Creates or replaces multiple synonyms in Algolia. |
| [Delete a Synonym](actions/delete-a-synonym.md) | DELETE | Deletes an existing synonym from Algolia. |
| [Delete All Synonyms](actions/delete-all-synonyms.md) | DELETE | Deletes all synonyms from an Algolia index. |
| [Retrieve a Synonym](actions/retrieve-a-synonym.md) | GET | Retrieves an existing synonym from Algolia. |
| [Search for Synonyms](actions/search-for-synonyms.md) | GET | Searches for synonyms in an Algolia index. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Check Application Task Status](actions/check-application-task-status.md) | GET | Retrieves an application task status from Algolia. |
| [Check Task Status](actions/check-task-status.md) | GET | Retrieves a task status from Algolia. |

