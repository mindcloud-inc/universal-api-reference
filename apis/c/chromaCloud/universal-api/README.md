# <img src="https://images.mindcloud.co/apps/icons/chroma-cloud_1776198311701.png" alt="Chroma Cloud logo" width="28" height="28"> Chroma Cloud: Universal API

Chroma Cloud is a hosted vector database and search platform for storing collections, records, embeddings, and sync sources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chromaCloud/latest
- **Category:** IT Operations / Database
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://trychroma.com
- **Vendor API docs:** https://docs.trychroma.com/cloud/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get user identity](actions/get-user-identity.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/get-user-identity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Attached Function

| Action | Method | Description |
| --- | --- | --- |
| [Attach function](actions/attach-function.md) | POST | Attaches a function to a collection in Chroma Cloud. |
| [Detach function](actions/detach-function.md) | DELETE | Detaches a function from a collection in Chroma Cloud. |
| [Get attached function](actions/get-attached-function.md) | GET | Retrieves an attached function from Chroma Cloud. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create collection](actions/create-collection.md) | POST | Creates a collection in Chroma Cloud. |
| [Delete collection](actions/delete-collection.md) | DELETE | Deletes a collection from Chroma Cloud. |
| [Get collection](actions/get-collection.md) | GET | Retrieves a collection from Chroma Cloud. |
| [Get collection by ID](actions/get-collection-by-id.md) | GET | Retrieves a collection by ID from Chroma Cloud. |
| [Get number of collections](actions/get-number-of-collections.md) | GET | Retrieves a collection count from Chroma Cloud. |
| [List collections](actions/list-collections.md) | GET | Retrieves collections from Chroma Cloud. |
| [Update collection](actions/update-collection.md) | PUT | Updates a collection in Chroma Cloud. |

### Collection Fork

| Action | Method | Description |
| --- | --- | --- |
| [Fork collection](actions/fork-collection.md) | POST | Creates a fork of a collection in Chroma Cloud. |
| [Get fork count](actions/get-fork-count.md) | GET | Retrieves a collection fork count from Chroma Cloud. |

### Collection Indexing

| Action | Method | Description |
| --- | --- | --- |
| [Get indexing status](actions/get-indexing-status.md) | GET | Retrieves collection indexing status from Chroma Cloud. |

### Collection Query

| Action | Method | Description |
| --- | --- | --- |
| [Query collection](actions/query-collection.md) | GET | Queries a collection in Chroma Cloud. |

### Database

| Action | Method | Description |
| --- | --- | --- |
| [Create database](actions/create-database.md) | POST | Creates a database in Chroma Cloud. |
| [Delete database](actions/delete-database.md) | DELETE | Deletes a database from Chroma Cloud. |
| [Get database](actions/get-database.md) | GET | Retrieves a database from Chroma Cloud. |
| [List databases](actions/list-databases.md) | GET | Retrieves databases from Chroma Cloud. |

### Invocation

| Action | Method | Description |
| --- | --- | --- |
| [Cancel invocation](actions/cancel-invocation.md) | PUT | Cancels an invocation in Chroma Cloud. |
| [Create invocation](actions/create-invocation.md) | POST | Creates an invocation in Chroma Cloud. |
| [Get invocation](actions/get-invocation.md) | GET | Retrieves an invocation from Chroma Cloud. |
| [Get latest invocations by keys](actions/get-latest-invocations-by-keys.md) | GET | Retrieves the latest invocations by key from Chroma Cloud. |
| [List invocations](actions/list-invocations.md) | GET | Retrieves invocations from Chroma Cloud. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Add records](actions/add-records.md) | POST | Adds records to a collection in Chroma Cloud. |
| [Delete records](actions/delete-records.md) | DELETE | Deletes records from a collection in Chroma Cloud. |
| [Get number of records](actions/get-number-of-records.md) | GET | Retrieves a collection record count from Chroma Cloud. |
| [Get records](actions/get-records.md) | GET | Retrieves records from a collection in Chroma Cloud. |
| [Update records](actions/update-records.md) | PUT | Updates records in a collection in Chroma Cloud. |
| [Upsert records](actions/upsert-records.md) | PUT | Updates records in Chroma Cloud, or creates them if absent. |

### Search

| Action | Method | Description |
| --- | --- | --- |
| [Search records](actions/search-records.md) | GET | Searches records in a collection in Chroma Cloud. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [Create source](actions/create-source.md) | POST | Creates a source in Chroma Cloud. |
| [Delete source](actions/delete-source.md) | DELETE | Deletes a source from Chroma Cloud. |
| [Get source](actions/get-source.md) | GET | Retrieves a source from Chroma Cloud. |
| [List sources](actions/list-sources.md) | GET | Retrieves sources from Chroma Cloud. |

### System

| Action | Method | Description |
| --- | --- | --- |
| [Get version](actions/get-version.md) | GET | Retrieves the Chroma Cloud version. |
| [Pre-flight checks](actions/pre-flight-checks.md) | GET | Retrieves pre-flight checks from Chroma Cloud. |

### Tenant

| Action | Method | Description |
| --- | --- | --- |
| [Create tenant](actions/create-tenant.md) | POST | Creates a tenant in Chroma Cloud. |
| [Get tenant](actions/get-tenant.md) | GET | Retrieves a tenant from Chroma Cloud. |
| [Update tenant](actions/update-tenant.md) | PUT | Updates a tenant in Chroma Cloud. |

### User Identity

| Action | Method | Description |
| --- | --- | --- |
| [Get user identity](actions/get-user-identity.md) | GET | Retrieves the current user identity from Chroma Cloud. |

