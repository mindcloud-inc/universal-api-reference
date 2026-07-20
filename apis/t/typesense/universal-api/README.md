# <img src="https://images.mindcloud.co/apps/icons/typesense-icon_1776796422589.png" alt="Typesense logo" width="28" height="28"> Typesense: Universal API

Manage Typesense collections, documents, searches, API keys, aliases, synonyms, curations, stopwords, analytics, and cluster operations through the Typesense Server API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/typesense/latest
- **Category:** IT Operations / Database
- **Actions:** 89
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://typesense.org/
- **Vendor API docs:** https://typesense.org/docs/30.0/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Health](actions/get-health.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typesense/latest/actions/get-health?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (89)

### Alias

| Action | Method | Description |
| --- | --- | --- |
| [Delete Alias](actions/delete-alias.md) | DELETE | Deletes a collection alias from Typesense. |
| [Get Alias](actions/get-alias.md) | GET | Retrieves a collection alias from Typesense. |
| [List Aliases](actions/list-aliases.md) | GET | Retrieves all collection aliases from Typesense. |
| [Upsert Alias](actions/upsert-alias.md) | PUT | Creates or updates a collection alias in Typesense. |

### Analytics Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Analytics Event](actions/create-analytics-event.md) | POST | Creates an analytics event in Typesense. |
| [Get Analytics Events](actions/get-analytics-events.md) | GET | Retrieves recent analytics events from Typesense. |

### Analytics Rule

| Action | Method | Description |
| --- | --- | --- |
| [Create Analytics Rules](actions/create-analytics-rules.md) | POST | Creates an analytics rule in Typesense. |
| [Delete Analytics Rule](actions/delete-analytics-rule.md) | DELETE | Deletes an analytics rule from Typesense. |
| [Get Analytics Rule](actions/get-analytics-rule.md) | GET | Retrieves an analytics rule from Typesense. |
| [List Analytics Rules](actions/list-analytics-rules.md) | GET | Retrieves all analytics rules from Typesense. |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Create API Key](actions/create-api-key.md) | POST | Creates a new API key in Typesense. |
| [Delete API Key](actions/delete-api-key.md) | DELETE | Deletes an API key from Typesense. |
| [Get API Key](actions/get-api-key.md) | GET | Retrieves an API key from Typesense. |
| [List API Keys](actions/list-api-keys.md) | GET | Retrieves all API keys from Typesense. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Clone Collection](actions/clone-collection.md) | POST | Creates a collection by cloning another in Typesense. |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in Typesense. |
| [Delete Collection](actions/delete-collection.md) | DELETE | Deletes a specific collection from Typesense. |
| [Get Collection](actions/get-collection.md) | GET | Retrieves a specific collection from Typesense. |
| [List Collections](actions/list-collections.md) | GET | Retrieves all available collections from Typesense. |
| [Update Collection Schema](actions/update-collection-schema.md) | PUT | Updates a collection schema in Typesense. |

### Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Get Configuration](actions/get-configuration.md) | GET | Retrieves current cluster configuration from Typesense. |
| [Update Configuration](actions/update-configuration.md) | PUT | Updates the current configuration in Typesense. |

### Conversation Model

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation Model](actions/create-conversation-model.md) | POST | Creates a conversation model in Typesense. |
| [Delete Conversation Model](actions/delete-conversation-model.md) | DELETE | Deletes a conversation model from Typesense. |
| [Get Conversation Model](actions/get-conversation-model.md) | GET | Retrieves a conversation model from Typesense. |
| [List Conversation Models](actions/list-conversation-models.md) | GET | Retrieves all conversation models from Typesense. |
| [Update Conversation Model](actions/update-conversation-model.md) | PUT | Updates a conversation model in Typesense. |

### Conversation Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Conversation Multi Search](actions/conversation-multi-search.md) | GET | Finds results in Typesense using conversational multi search. |

### Curation Item

| Action | Method | Description |
| --- | --- | --- |
| [Delete Curation Item](actions/delete-curation-item.md) | DELETE | Deletes a specific curation from Typesense. |
| [Get Curation Item](actions/get-curation-item.md) | GET | Retrieves a curation from a Typesense curation set. |
| [List Curation Items](actions/list-curation-items.md) | GET | Retrieves curations from a Typesense curation set. |
| [Upsert Curation Item](actions/upsert-curation-item.md) | PUT | Creates or updates a curation in Typesense. |

### Curation Set

| Action | Method | Description |
| --- | --- | --- |
| [Delete Curation Set](actions/delete-curation-set.md) | DELETE | Deletes a curation set from Typesense. |
| [Get Curation Set](actions/get-curation-set.md) | GET | Retrieves a curation set from Typesense. |
| [List Curation Sets](actions/list-curation-sets.md) | GET | Retrieves all curation sets from Typesense. |
| [Upsert Curation Set](actions/upsert-curation-set.md) | PUT | Creates or updates a curation set in Typesense. |

### Debug Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Debug Info](actions/get-debug-info.md) | GET | Retrieves current debug information from Typesense. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a new document in Typesense. |
| [Delete All Documents](actions/delete-all-documents.md) | DELETE | Deletes all documents from a Typesense collection. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a specific document from Typesense. |
| [Delete Documents By Query](actions/delete-documents-by-query.md) | DELETE | Deletes matching documents from a Typesense collection. |
| [Get Document](actions/get-document.md) | GET | Retrieves a specific document from Typesense. |
| [Update Document](actions/update-document.md) | PUT | Updates an existing document in Typesense. |
| [Update Documents By Query](actions/update-documents-by-query.md) | PUT | Updates matching documents in a Typesense collection. |
| [Upsert Document](actions/upsert-document.md) | PUT | Creates or updates a document in Typesense. |

### Document Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Documents](actions/export-documents.md) | GET | Exports documents from a Typesense collection. |

### Document Import

| Action | Method | Description |
| --- | --- | --- |
| [Import Documents](actions/import-documents.md) | POST | Imports documents into a Typesense collection. |
| [Import Documents With Emplace](actions/import-documents-with-emplace.md) | PUT | Imports documents into Typesense using emplace mode. |
| [Import Documents With Update](actions/import-documents-with-update.md) | PUT | Imports documents into Typesense using update mode. |
| [Import Documents With Upsert](actions/import-documents-with-upsert.md) | PUT | Imports documents into Typesense using upsert mode. |

### Embedding

| Action | Method | Description |
| --- | --- | --- |
| [Create Embeddings](actions/create-embeddings.md) | POST | Creates new vector embeddings in Typesense. |

### Health

| Action | Method | Description |
| --- | --- | --- |
| [Get Health](actions/get-health.md) | GET | Retrieves current cluster health from Typesense. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Metrics](actions/get-metrics.md) | GET | Retrieves current cluster metrics from Typesense. |

### Natural Language Search Model

| Action | Method | Description |
| --- | --- | --- |
| [Create Natural Language Search Model](actions/create-natural-language-search-model.md) | POST | Creates a natural language search model in Typesense. |
| [Delete Natural Language Search Model](actions/delete-natural-language-search-model.md) | DELETE | Deletes a natural language search model from Typesense. |
| [Get Natural Language Search Model](actions/get-natural-language-search-model.md) | GET | Retrieves a natural language search model from Typesense. |
| [List Natural Language Search Models](actions/list-natural-language-search-models.md) | GET | Retrieves natural language search models from Typesense. |
| [Update Natural Language Search Model](actions/update-natural-language-search-model.md) | PUT | Updates a natural language search model in Typesense. |

### Operation

| Action | Method | Description |
| --- | --- | --- |
| [Clear Cache](actions/clear-cache.md) | PUT | Clears the current server cache in Typesense. |
| [Compact Database](actions/compact-database.md) | PUT | Compacts the current database in Typesense. |
| [Create Snapshot](actions/create-snapshot.md) | POST | Creates a backup snapshot in Typesense. |
| [Trigger Leader Election](actions/trigger-leader-election.md) | PUT | Triggers a leader election in Typesense. |

### Preset

| Action | Method | Description |
| --- | --- | --- |
| [Delete Preset](actions/delete-preset.md) | DELETE | Deletes a search preset from Typesense. |
| [Get Preset](actions/get-preset.md) | GET | Retrieves a search preset from Typesense. |
| [List Presets](actions/list-presets.md) | GET | Retrieves all search presets from Typesense. |
| [Upsert Preset](actions/upsert-preset.md) | PUT | Creates or updates a search preset in Typesense. |

### Schema Change

| Action | Method | Description |
| --- | --- | --- |
| [List Schema Changes](actions/list-schema-changes.md) | GET | Retrieves collection schema changes from Typesense. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Multi Search](actions/multi-search.md) | GET | Finds results in Typesense across multiple searches. |
| [Natural Language Search Documents](actions/natural-language-search-documents.md) | GET | Finds documents in Typesense using natural language search. |
| [Search Documents](actions/search-documents.md) | GET | Finds documents in Typesense by search query. |

### Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Stats](actions/get-stats.md) | GET | Retrieves current cluster stats from Typesense. |

### Stemming Dictionary

| Action | Method | Description |
| --- | --- | --- |
| [Delete Stemming Dictionary](actions/delete-stemming-dictionary.md) | DELETE | Deletes a stemming dictionary from Typesense. |
| [Get Stemming Dictionary](actions/get-stemming-dictionary.md) | GET | Retrieves a stemming dictionary from Typesense. |
| [Import Stemming Dictionary](actions/import-stemming-dictionary.md) | POST | Imports a stemming dictionary into Typesense. |
| [List Stemming Dictionaries](actions/list-stemming-dictionaries.md) | GET | Retrieves all stemming dictionaries from Typesense. |

### Stopwords Set

| Action | Method | Description |
| --- | --- | --- |
| [Delete Stopwords Set](actions/delete-stopwords-set.md) | DELETE | Deletes a stopwords set from Typesense. |
| [Get Stopwords Set](actions/get-stopwords-set.md) | GET | Retrieves a stopwords set from Typesense. |
| [List Stopwords Sets](actions/list-stopwords-sets.md) | GET | Retrieves all stopwords sets from Typesense. |
| [Upsert Stopwords Set](actions/upsert-stopwords-set.md) | PUT | Creates or updates a stopwords set in Typesense. |

### Synonym Item

| Action | Method | Description |
| --- | --- | --- |
| [Delete Synonym Item](actions/delete-synonym-item.md) | DELETE | Deletes a specific synonym from Typesense. |
| [Get Synonym Item](actions/get-synonym-item.md) | GET | Retrieves a synonym from a Typesense synonym set. |
| [List Synonym Items](actions/list-synonym-items.md) | GET | Retrieves synonyms from a Typesense synonym set. |
| [Upsert Synonym Item](actions/upsert-synonym-item.md) | PUT | Creates or updates a synonym in Typesense. |

### Synonym Set

| Action | Method | Description |
| --- | --- | --- |
| [Delete Synonym Set](actions/delete-synonym-set.md) | DELETE | Deletes a synonym set from Typesense. |
| [Get Synonym Set](actions/get-synonym-set.md) | GET | Retrieves a synonym set from Typesense. |
| [List Synonym Sets](actions/list-synonym-sets.md) | GET | Retrieves all synonym sets from Typesense. |
| [Upsert Synonym Set](actions/upsert-synonym-set.md) | PUT | Creates or updates a synonym set in Typesense. |

### Vector Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Vector Search Documents](actions/vector-search-documents.md) | GET | Finds documents in Typesense using vector search. |

### Voice Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Voice Multi Search](actions/voice-multi-search.md) | GET | Finds results in Typesense using voice query search. |

