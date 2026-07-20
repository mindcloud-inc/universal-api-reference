# Typesense: Native API Reference

A consolidated summary of Typesense's API configuration and 89 documented operations, with links to official documentation.

- **Official docs:** https://typesense.org/docs/30.0/api/
- **API base URL:** `https://5brh8vz1lictf0jop-1.a2.typesense.net`

## Authentication

### Typesense API Key

Uses a Typesense Server API key sent in the X-TYPESENSE-API-KEY header.

### Credentials

- **API Key:** `apiKey` · required · Typesense Server API key sent as the X-TYPESENSE-API-KEY request header.

Send these headers with each API request:

```http
X-TYPESENSE-API-KEY: <apiKey>
```

[Official authentication documentation](https://typesense.org/docs/30.0/api/authentication.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Filtering

Send filters in the query string. Supported operators: `contains`, `equals`.

## Sorting

Set the sort field with `sort_by` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `408,429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (89 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Clear Cache](actions/clear-cache.md) | `POST /operations/cache/clear` | [docs](https://typesense.org/docs/30.0/api/cluster-operations.html#clear-cache) |
| [Clone Collection](actions/clone-collection.md) | `POST /collections` | [docs](https://typesense.org/docs/30.0/api/collections.html#clone-a-collection) |
| [Compact Database](actions/compact-database.md) | `POST /operations/db/compact` | [docs](https://typesense.org/docs/30.0/api/cluster-operations.html#compact-db) |
| [Conversation Multi Search](actions/conversation-multi-search.md) | `POST /multi_search` | [docs](https://typesense.org/docs/30.0/api/conversational-search-rag.html) |
| [Create Analytics Event](actions/create-analytics-event.md) | `POST /analytics/events` | [docs](https://typesense.org/docs/30.0/api/analytics-query-suggestions.html#send-events-via-api) |
| [Create Analytics Rules](actions/create-analytics-rules.md) | `POST /analytics/rules` | [docs](https://typesense.org/docs/30.0/api/analytics-query-suggestions.html#create-analytics-rules) |
| [Create API Key](actions/create-api-key.md) | `POST /keys` | [docs](https://typesense.org/docs/30.0/api/api-keys.html#create-an-api-key) |
| [Create Collection](actions/create-collection.md) | `POST /collections` | [docs](https://typesense.org/docs/30.0/api/collections.html#create-a-collection) |
| [Create Conversation Model](actions/create-conversation-model.md) | `POST /conversations/models` | [docs](https://typesense.org/docs/30.0/api/conversational-search-rag.html#create-a-conversation-model) |
| [Create Document](actions/create-document.md) | `POST /collections/{{collection}}/documents` | [docs](https://typesense.org/docs/30.0/api/documents.html#index-a-document) |
| [Create Embeddings](actions/create-embeddings.md) | `POST /v1/embeddings` | [docs](https://typesense.org/docs/30.0/api/vector-search.html#generating-embeddings) |
| [Create Natural Language Search Model](actions/create-natural-language-search-model.md) | `POST /nl_search_models` | [docs](https://typesense.org/docs/30.0/api/natural-language-search.html#create-a-natural-language-search-model) |
| [Create Snapshot](actions/create-snapshot.md) | `POST /operations/snapshot` | [docs](https://typesense.org/docs/30.0/api/cluster-operations.html#create-snapshot-for-backups) |
| [Delete Alias](actions/delete-alias.md) | `DELETE /aliases/{{alias}}` | [docs](https://typesense.org/docs/30.0/api/collection-alias.html#delete-an-alias) |
| [Delete All Documents](actions/delete-all-documents.md) | `DELETE /collections/{{collection}}/documents` | [docs](https://typesense.org/docs/30.0/api/documents.html#delete-all-documents) |
| [Delete Analytics Rule](actions/delete-analytics-rule.md) | `DELETE /analytics/rules/{{name}}` | [docs](https://typesense.org/docs/30.0/api/analytics-query-suggestions.html#remove-a-rule) |
| [Delete API Key](actions/delete-api-key.md) | `DELETE /keys/{{id}}` | [docs](https://typesense.org/docs/30.0/api/api-keys.html#delete-api-key) |
| [Delete Collection](actions/delete-collection.md) | `DELETE /collections/{{collection}}` | [docs](https://typesense.org/docs/30.0/api/collections.html#drop-a-collection) |
| [Delete Conversation Model](actions/delete-conversation-model.md) | `DELETE /conversations/models/{{modelId}}` | [docs](https://typesense.org/docs/30.0/api/conversational-search-rag.html#managing-conversation-models) |
| [Delete Curation Item](actions/delete-curation-item.md) | `DELETE /curation_sets/{{name}}/items/{{id}}` | [docs](https://typesense.org/docs/30.0/api/curation.html#delete-a-curation) |
| [Delete Curation Set](actions/delete-curation-set.md) | `DELETE /curation_sets/{{name}}` | [docs](https://typesense.org/docs/30.0/api/curation.html#delete-a-curation-set) |
| [Delete Document](actions/delete-document.md) | `DELETE /collections/{{collection}}/documents/{{id}}` | [docs](https://typesense.org/docs/30.0/api/documents.html#delete-a-document) |
| [Delete Documents By Query](actions/delete-documents-by-query.md) | `DELETE /collections/{{collection}}/documents` | [docs](https://typesense.org/docs/30.0/api/documents.html#delete-documents-by-query) |
| [Delete Natural Language Search Model](actions/delete-natural-language-search-model.md) | `DELETE /nl_search_models/{{modelId}}` | [docs](https://typesense.org/docs/30.0/api/natural-language-search.html#delete-model) |
| [Delete Preset](actions/delete-preset.md) | `DELETE /presets/{{presetName}}` | [docs](https://typesense.org/docs/30.0/api/api-keys.html#preset-operations) |
| [Delete Stemming Dictionary](actions/delete-stemming-dictionary.md) | `DELETE /stemming/dictionaries/{{id}}` | [docs](https://typesense.org/docs/30.0/api/api-keys.html#stemming-dictionary-operations) |
| [Delete Stopwords Set](actions/delete-stopwords-set.md) | `DELETE /stopwords/{{setId}}` | [docs](https://typesense.org/docs/30.0/api/api-keys.html#stopwords-actions) |
| [Delete Synonym Item](actions/delete-synonym-item.md) | `DELETE /synonym_sets/{{synonymSetName}}/items/{{id}}` | [docs](https://typesense.org/docs/30.0/api/synonyms.html#delete-a-synonym) |
| [Delete Synonym Set](actions/delete-synonym-set.md) | `DELETE /synonym_sets/{{synonymSetName}}` | [docs](https://typesense.org/docs/30.0/api/synonyms.html#delete-a-synonym-set) |
| [Export Documents](actions/export-documents.md) | `GET /collections/{{collection}}/documents/export` | [docs](https://typesense.org/docs/30.0/api/documents.html#export-documents) |
| [Get Alias](actions/get-alias.md) | `GET /aliases/{{alias}}` | [docs](https://typesense.org/docs/30.0/api/collection-alias.html#retrieve-an-alias) |
| [Get Analytics Events](actions/get-analytics-events.md) | `GET /analytics/events` | [docs](https://typesense.org/docs/30.0/api/analytics-query-suggestions.html#send-events-via-api) |
| [Get Analytics Rule](actions/get-analytics-rule.md) | `GET /analytics/rules/{{name}}` | [docs](https://typesense.org/docs/30.0/api/analytics-query-suggestions.html#create-analytics-rules) |
| [Get API Key](actions/get-api-key.md) | `GET /keys/{{id}}` | [docs](https://typesense.org/docs/30.0/api/api-keys.html#retrieve-an-api-key) |
| [Get Collection](actions/get-collection.md) | `GET /collections/{{collection}}` | [docs](https://typesense.org/docs/30.0/api/collections.html#retrieve-a-collection) |
| [Get Configuration](actions/get-configuration.md) | `GET /config` | [docs](https://typesense.org/docs/30.0/api/cluster-operations.html#config) |
| [Get Conversation Model](actions/get-conversation-model.md) | `GET /conversations/models/{{modelId}}` | [docs](https://typesense.org/docs/30.0/api/conversational-search-rag.html#retrieve-a-single-model) |
| [Get Curation Item](actions/get-curation-item.md) | `GET /curation_sets/{{name}}/items/{{id}}` | [docs](https://typesense.org/docs/30.0/api/curation.html#retrieve-a-curation) |
| [Get Curation Set](actions/get-curation-set.md) | `GET /curation_sets/{{name}}` | [docs](https://typesense.org/docs/30.0/api/curation.html#retrieve-a-curation-set) |
| [Get Debug Info](actions/get-debug-info.md) | `GET /debug` | [docs](https://typesense.org/docs/30.0/api/cluster-operations.html#debug) |
| [Get Document](actions/get-document.md) | `GET /collections/{{collection}}/documents/{{id}}` | [docs](https://typesense.org/docs/30.0/api/documents.html#retrieve-a-document) |
| [Get Health](actions/get-health.md) | `GET /health` | [docs](https://typesense.org/docs/30.0/api/cluster-operations.html#health) |
| [Get Metrics](actions/get-metrics.md) | `GET /metrics.json` | [docs](https://typesense.org/docs/30.0/api/cluster-operations.html#metrics) |
| [Get Natural Language Search Model](actions/get-natural-language-search-model.md) | `GET /nl_search_models/{{modelId}}` | [docs](https://typesense.org/docs/30.0/api/natural-language-search.html#get-model-details) |
| [Get Preset](actions/get-preset.md) | `GET /presets/{{presetName}}` | [docs](https://typesense.org/docs/30.0/api/search.html#search-parameters) |
| [Get Stats](actions/get-stats.md) | `GET /stats.json` | [docs](https://typesense.org/docs/30.0/api/cluster-operations.html#stats) |
| [Get Stemming Dictionary](actions/get-stemming-dictionary.md) | `GET /stemming/dictionaries/{{id}}` | [docs](https://typesense.org/docs/30.0/api/stemming.html#managing-dictionaries) |
| [Get Stopwords Set](actions/get-stopwords-set.md) | `GET /stopwords/{{setId}}` | [docs](https://typesense.org/docs/30.0/api/stopwords.html#get-a-specific-stopwords-set) |
| [Get Synonym Item](actions/get-synonym-item.md) | `GET /synonym_sets/{{synonymSetName}}/items/{{id}}` | [docs](https://typesense.org/docs/30.0/api/synonyms.html#retrieve-a-synonym) |
| [Get Synonym Set](actions/get-synonym-set.md) | `GET /synonym_sets/{{synonymSetName}}` | [docs](https://typesense.org/docs/30.0/api/synonyms.html#retrieve-a-synonym-set) |
| [Import Documents](actions/import-documents.md) | `POST /collections/{{collection}}/documents/import` | [docs](https://typesense.org/docs/30.0/api/documents.html#import-documents) |
| [Import Documents With Emplace](actions/import-documents-with-emplace.md) | `POST /collections/{{collection}}/documents/import` | [docs](https://typesense.org/docs/30.0/api/documents.html#action-modes-batch-create-upsert-update-emplace) |
| [Import Documents With Update](actions/import-documents-with-update.md) | `POST /collections/{{collection}}/documents/import` | [docs](https://typesense.org/docs/30.0/api/documents.html#action-modes-batch-create-upsert-update-emplace) |
| [Import Documents With Upsert](actions/import-documents-with-upsert.md) | `POST /collections/{{collection}}/documents/import` | [docs](https://typesense.org/docs/30.0/api/documents.html#action-modes-batch-create-upsert-update-emplace) |
| [Import Stemming Dictionary](actions/import-stemming-dictionary.md) | `POST /stemming/dictionaries/import` | [docs](https://typesense.org/docs/30.0/api/stemming.html#creating-a-stemming-dictionary) |
| [List Aliases](actions/list-aliases.md) | `GET /aliases` | [docs](https://typesense.org/docs/30.0/api/collection-alias.html#list-all-aliases) |
| [List Analytics Rules](actions/list-analytics-rules.md) | `GET /analytics/rules` | [docs](https://typesense.org/docs/30.0/api/analytics-query-suggestions.html#create-analytics-rules) |
| [List API Keys](actions/list-api-keys.md) | `GET /keys` | [docs](https://typesense.org/docs/30.0/api/api-keys.html#list-all-keys) |
| [List Collections](actions/list-collections.md) | `GET /collections` | [docs](https://typesense.org/docs/30.0/api/collections.html#list-collections) |
| [List Conversation Models](actions/list-conversation-models.md) | `GET /conversations/models` | [docs](https://typesense.org/docs/30.0/api/conversational-search-rag.html#retrieve-all-models) |
| [List Curation Items](actions/list-curation-items.md) | `GET /curation_sets/{{name}}/items` | [docs](https://typesense.org/docs/30.0/api/curation.html#list-curations-in-a-set) |
| [List Curation Sets](actions/list-curation-sets.md) | `GET /curation_sets` | [docs](https://typesense.org/docs/30.0/api/curation.html#list-all-curation-sets) |
| [List Natural Language Search Models](actions/list-natural-language-search-models.md) | `GET /nl_search_models` | [docs](https://typesense.org/docs/30.0/api/natural-language-search.html#list-all-models) |
| [List Presets](actions/list-presets.md) | `GET /presets` | [docs](https://typesense.org/docs/30.0/api/api-keys.html#preset-operations) |
| [List Schema Changes](actions/list-schema-changes.md) | `GET /operations/schema_changes` | [docs](https://typesense.org/docs/30.0/api/collections.html#alter-a-collection) |
| [List Stemming Dictionaries](actions/list-stemming-dictionaries.md) | `GET /stemming/dictionaries` | [docs](https://typesense.org/docs/30.0/api/stemming.html#managing-dictionaries) |
| [List Stopwords Sets](actions/list-stopwords-sets.md) | `GET /stopwords` | [docs](https://typesense.org/docs/30.0/api/stopwords.html#getting-all-stopwords-sets) |
| [List Synonym Items](actions/list-synonym-items.md) | `GET /synonym_sets/{{synonymSetName}}/items` | [docs](https://typesense.org/docs/30.0/api/synonyms.html#list-synonyms-in-a-set) |
| [List Synonym Sets](actions/list-synonym-sets.md) | `GET /synonym_sets` | [docs](https://typesense.org/docs/30.0/api/synonyms.html#list-all-synonym-sets) |
| [Multi Search](actions/multi-search.md) | `POST /multi_search` | [docs](https://typesense.org/docs/30.0/api/federated-multi-search.html#multi-search) |
| [Natural Language Search Documents](actions/natural-language-search-documents.md) | `GET /collections/{{collection}}/documents/search` | [docs](https://typesense.org/docs/30.0/api/natural-language-search.html) |
| [Search Documents](actions/search-documents.md) | `GET /collections/{{collection}}/documents/search` | [docs](https://typesense.org/docs/30.0/api/search.html#search-parameters) |
| [Trigger Leader Election](actions/trigger-leader-election.md) | `POST /operations/vote` | [docs](https://typesense.org/docs/30.0/api/cluster-operations.html#trigger-leader-election) |
| [Update Collection Schema](actions/update-collection-schema.md) | `PATCH /collections/{{collection}}` | [docs](https://typesense.org/docs/30.0/api/collections.html#alter-a-collection) |
| [Update Configuration](actions/update-configuration.md) | `POST /config` | [docs](https://typesense.org/docs/30.0/api/cluster-operations.html#config) |
| [Update Conversation Model](actions/update-conversation-model.md) | `PUT /conversations/models/{{modelId}}` | [docs](https://typesense.org/docs/30.0/api/conversational-search-rag.html#managing-conversation-models) |
| [Update Document](actions/update-document.md) | `PATCH /collections/{{collection}}/documents/{{id}}` | [docs](https://typesense.org/docs/30.0/api/documents.html#update-a-document) |
| [Update Documents By Query](actions/update-documents-by-query.md) | `PATCH /collections/{{collection}}/documents` | [docs](https://typesense.org/docs/30.0/api/documents.html#update-documents-by-query) |
| [Update Natural Language Search Model](actions/update-natural-language-search-model.md) | `PUT /nl_search_models/{{modelId}}` | [docs](https://typesense.org/docs/30.0/api/natural-language-search.html#update-model) |
| [Upsert Alias](actions/upsert-alias.md) | `PUT /aliases/{{alias}}` | [docs](https://typesense.org/docs/30.0/api/collection-alias.html#create-or-update-an-alias) |
| [Upsert Curation Item](actions/upsert-curation-item.md) | `PUT /curation_sets/{{name}}/items/{{id}}` | [docs](https://typesense.org/docs/30.0/api/curation.html#create-or-update-a-curation) |
| [Upsert Curation Set](actions/upsert-curation-set.md) | `PUT /curation_sets/{{name}}` | [docs](https://typesense.org/docs/30.0/api/api-keys.html#curation-set-actions) |
| [Upsert Document](actions/upsert-document.md) | `POST /collections/{{collection}}/documents` | [docs](https://typesense.org/docs/30.0/api/documents.html#upsert-a-single-document) |
| [Upsert Preset](actions/upsert-preset.md) | `PUT /presets/{{presetName}}` | [docs](https://typesense.org/docs/30.0/api/search.html#presets) |
| [Upsert Stopwords Set](actions/upsert-stopwords-set.md) | `PUT /stopwords/{{setId}}` | [docs](https://typesense.org/docs/30.0/api/stopwords.html#adding-stopwords) |
| [Upsert Synonym Item](actions/upsert-synonym-item.md) | `PUT /synonym_sets/{{synonymSetName}}/items/{{id}}` | [docs](https://typesense.org/docs/30.0/api/synonyms.html#create-or-update-a-synonym) |
| [Upsert Synonym Set](actions/upsert-synonym-set.md) | `PUT /synonym_sets/{{synonymSetName}}` | [docs](https://typesense.org/docs/30.0/api/synonyms.html#create-or-update-a-synonym-set) |
| [Vector Search Documents](actions/vector-search-documents.md) | `GET /collections/{{collection}}/documents/search` | [docs](https://typesense.org/docs/30.0/api/vector-search.html) |
| [Voice Multi Search](actions/voice-multi-search.md) | `POST /multi_search` | [docs](https://typesense.org/docs/30.0/api/voice-search.html) |
