# Milvus Vector Store: Native API Reference

A consolidated summary of Milvus Vector Store's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.zilliz.com/reference/restful/data-plane-v2
- **API base URL:** `https://{clusterEndpoint}`

## Authentication

### API Key

Use a Zilliz Cloud API key with a cluster endpoint to access Milvus data-plane APIs.

### Credentials

- **API Key:** `apiKey` · required
- **Cluster Endpoint:** `clusterEndpoint` · required · Cluster endpoint host for the target Zilliz Cloud cluster, without the https:// prefix. You can copy it from Zilliz Cloud cluster details or the Describe Cluster API response.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.zilliz.com/reference/restful/data-plane-v2)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Alter Alias](actions/alter-alias.md) | `POST /v2/vectordb/aliases/alter` | [docs](https://docs.zilliz.com/reference/restful/alter-alias-v2) |
| [Alter Collection Properties](actions/alter-collection-properties.md) | `POST /v2/vectordb/collections/alter_properties` | [docs](https://docs.zilliz.com/reference/restful/alter-collection-properties-v2) |
| [Alter Database Properties](actions/alter-database-properties.md) | `POST /v2/vectordb/databases/alter_properties` | [docs](https://docs.zilliz.com/reference/restful/alter-database-properties-v2) |
| [Alter Index Properties](actions/alter-index-properties.md) | `POST /v2/vectordb/indexes/alter_properties` | [docs](https://docs.zilliz.com/reference/restful/alter-index-properties-v2) |
| [Compact Collection](actions/compact-collection.md) | `POST /v2/vectordb/collections/compact` | [docs](https://docs.zilliz.com/reference/restful/compact-collection-v2) |
| [Create Alias](actions/create-alias.md) | `POST /v2/vectordb/aliases/create` | [docs](https://docs.zilliz.com/reference/restful/create-alias-v2) |
| [Create Collection](actions/create-collection.md) | `POST /v2/vectordb/collections/create` | [docs](https://docs.zilliz.com/reference/restful/create-collection-v2) |
| [Create Database](actions/create-database.md) | `POST /v2/vectordb/databases/create` | [docs](https://docs.zilliz.com/reference/restful/create-database-v2) |
| [Create Index](actions/create-index.md) | `POST /v2/vectordb/indexes/create` | [docs](https://docs.zilliz.com/reference/restful/create-index-v2) |
| [Create Partition](actions/create-partition.md) | `POST /v2/vectordb/partitions/create` | [docs](https://docs.zilliz.com/reference/restful/create-partition-v2) |
| [Delete Vectors](actions/delete-vectors.md) | `POST /v2/vectordb/entities/delete` | [docs](https://docs.zilliz.com/reference/restful/delete-v2) |
| [Describe Alias](actions/describe-alias.md) | `POST /v2/vectordb/aliases/describe` | [docs](https://docs.zilliz.com/reference/restful/describe-alias-v2) |
| [Describe Collection](actions/describe-collection.md) | `POST /v2/vectordb/collections/describe` | [docs](https://docs.zilliz.com/reference/restful/describe-collection-v2) |
| [Describe Database](actions/describe-database.md) | `POST /v2/vectordb/databases/describe` | [docs](https://docs.zilliz.com/reference/restful/describe-database-v2) |
| [Describe Index](actions/describe-index.md) | `POST /v2/vectordb/indexes/describe` | [docs](https://docs.zilliz.com/reference/restful/describe-index-v2) |
| [Drop Alias](actions/drop-alias.md) | `POST /v2/vectordb/aliases/drop` | [docs](https://docs.zilliz.com/reference/restful/drop-alias-v2) |
| [Drop Collection](actions/drop-collection.md) | `POST /v2/vectordb/collections/drop` | [docs](https://docs.zilliz.com/reference/restful/drop-collection-v2) |
| [Drop Collection Properties](actions/drop-collection-properties.md) | `POST /v2/vectordb/collections/drop_properties` | [docs](https://docs.zilliz.com/reference/restful/drop-collection-properties-v2) |
| [Drop Database](actions/drop-database.md) | `POST /v2/vectordb/databases/drop` | [docs](https://docs.zilliz.com/reference/restful/drop-database-v2) |
| [Drop Database Properties](actions/drop-database-properties.md) | `POST /v2/vectordb/databases/drop_properties` | [docs](https://docs.zilliz.com/reference/restful/drop-database-properties-v2) |
| [Drop Index](actions/drop-index.md) | `POST /v2/vectordb/indexes/drop` | [docs](https://docs.zilliz.com/reference/restful/drop-index-v2) |
| [Drop Index Properties](actions/drop-index-properties.md) | `POST /v2/vectordb/indexes/drop_properties` | [docs](https://docs.zilliz.com/reference/restful/drop-index-properties-v2) |
| [Drop Partition](actions/drop-partition.md) | `POST /v2/vectordb/partitions/drop` | [docs](https://docs.zilliz.com/reference/restful/drop-partition-v2) |
| [Get Partition Statistics](actions/get-partition-statistics.md) | `POST /v2/vectordb/partitions/get_stats` | [docs](https://docs.zilliz.com/reference/restful/get-partition-statistics-v2) |
| [Get Vectors](actions/get-vectors.md) | `POST /v2/vectordb/entities/get` | [docs](https://docs.zilliz.com/reference/restful/get-v2) |
| [Has Collection](actions/has-collection.md) | `POST /v2/vectordb/collections/has` | [docs](https://docs.zilliz.com/reference/restful/has-collection-v2) |
| [Has Partition](actions/has-partition.md) | `POST /v2/vectordb/partitions/has` | [docs](https://docs.zilliz.com/reference/restful/has-partition-v2) |
| [Hybrid Search Vectors](actions/hybrid-search-vectors.md) | `POST /v2/vectordb/entities/hybrid_search` | [docs](https://docs.zilliz.com/reference/restful/hybrid-search-v2) |
| [Insert Vectors](actions/insert-vectors.md) | `POST /v2/vectordb/entities/insert` | [docs](https://docs.zilliz.com/reference/restful/insert-v2) |
| [List Aliases](actions/list-aliases.md) | `POST /v2/vectordb/aliases/list` | [docs](https://docs.zilliz.com/reference/restful/list-aliases-v2) |
| [List Collections](actions/list-collections.md) | `POST /v2/vectordb/collections/list` | [docs](https://docs.zilliz.com/reference/restful/list-collections-v2) |
| [List Databases](actions/list-databases.md) | `POST /v2/vectordb/databases/list` | [docs](https://docs.zilliz.com/reference/restful/list-databases-v2) |
| [List Indexes](actions/list-indexes.md) | `POST /v2/vectordb/indexes/list` | [docs](https://docs.zilliz.com/reference/restful/list-indexes-v2) |
| [List Partitions](actions/list-partitions.md) | `POST /v2/vectordb/partitions/list` | [docs](https://docs.zilliz.com/reference/restful/list-partitions-v2) |
| [Load Collection](actions/load-collection.md) | `POST /v2/vectordb/collections/load` | [docs](https://docs.zilliz.com/reference/restful/load-collection-v2) |
| [Query Vectors](actions/query-vectors.md) | `POST /v2/vectordb/entities/query` | [docs](https://docs.zilliz.com/reference/restful/query-v2) |
| [Release Collection](actions/release-collection.md) | `POST /v2/vectordb/collections/release` | [docs](https://docs.zilliz.com/reference/restful/release-collection-v2) |
| [Rename Collection](actions/rename-collection.md) | `POST /v2/vectordb/collections/rename` | [docs](https://docs.zilliz.com/reference/restful/rename-collection-v2) |
| [Search Vectors](actions/search-vectors.md) | `POST /v2/vectordb/entities/search` | [docs](https://docs.zilliz.com/reference/restful/search-v2) |
| [Upsert Vectors](actions/upsert-vectors.md) | `POST /v2/vectordb/entities/upsert` | [docs](https://docs.zilliz.com/reference/restful/upsert-v2) |
