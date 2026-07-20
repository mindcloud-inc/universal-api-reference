# <img src="https://images.mindcloud.co/apps/icons/milvus-vector-store_1775752012431.png" alt="Milvus Vector Store logo" width="28" height="28"> Milvus Vector Store: Universal API

Create databases, collections, indexes, partitions, aliases, users, and vector data operations in a Milvus-compatible Zilliz Cloud cluster.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/milvusVectorStore/latest
- **Category:** IT Operations / Database
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zilliz.com/cloud
- **Vendor API docs:** https://docs.zilliz.com/reference/restful/data-plane-v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Databases](actions/list-databases.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/milvusVectorStore/latest/actions/list-databases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Alias

| Action | Method | Description |
| --- | --- | --- |
| [Alter Alias](actions/alter-alias.md) | PUT | Updates an alias in Milvus Vector Store. |
| [Create Alias](actions/create-alias.md) | POST | Creates an alias in Milvus Vector Store. |
| [Describe Alias](actions/describe-alias.md) | GET | Retrieves alias details from Milvus Vector Store. |
| [Drop Alias](actions/drop-alias.md) | DELETE | Deletes an alias from Milvus Vector Store. |
| [List Aliases](actions/list-aliases.md) | GET | Retrieves aliases from Milvus Vector Store. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Alter Collection Properties](actions/alter-collection-properties.md) | PUT | Updates collection properties in Milvus Vector Store. |
| [Compact Collection](actions/compact-collection.md) | PUT | Compacts a collection in Milvus Vector Store. |
| [Create Collection](actions/create-collection.md) | POST | Creates a collection in Milvus Vector Store. |
| [Describe Collection](actions/describe-collection.md) | GET | Retrieves collection details from Milvus Vector Store. |
| [Drop Collection](actions/drop-collection.md) | DELETE | Deletes a collection from Milvus Vector Store. |
| [Drop Collection Properties](actions/drop-collection-properties.md) | PUT | Drops collection properties in Milvus Vector Store. |
| [Has Collection](actions/has-collection.md) | GET | Checks whether a collection exists in Milvus Vector Store. |
| [List Collections](actions/list-collections.md) | GET | Retrieves collections from Milvus Vector Store. |
| [Load Collection](actions/load-collection.md) | PUT | Loads a collection in Milvus Vector Store. |
| [Release Collection](actions/release-collection.md) | PUT | Releases a collection from memory in Milvus Vector Store. |
| [Rename Collection](actions/rename-collection.md) | PUT | Renames a collection in Milvus Vector Store. |

### Database

| Action | Method | Description |
| --- | --- | --- |
| [Alter Database Properties](actions/alter-database-properties.md) | PUT | Updates database properties in Milvus Vector Store. |
| [Create Database](actions/create-database.md) | POST | Creates a database in Milvus Vector Store. |
| [Describe Database](actions/describe-database.md) | GET | Retrieves database details from Milvus Vector Store. |
| [Drop Database](actions/drop-database.md) | DELETE | Deletes a database from Milvus Vector Store. |
| [Drop Database Properties](actions/drop-database-properties.md) | PUT | Drops database properties in Milvus Vector Store. |
| [List Databases](actions/list-databases.md) | GET | Retrieves databases from Milvus Vector Store. |

### Index

| Action | Method | Description |
| --- | --- | --- |
| [Alter Index Properties](actions/alter-index-properties.md) | PUT | Updates index properties in Milvus Vector Store. |
| [Create Index](actions/create-index.md) | POST | Creates an index in Milvus Vector Store. |
| [Describe Index](actions/describe-index.md) | GET | Retrieves index details from Milvus Vector Store. |
| [Drop Index](actions/drop-index.md) | DELETE | Deletes an index from Milvus Vector Store. |
| [Drop Index Properties](actions/drop-index-properties.md) | PUT | Drops index properties in Milvus Vector Store. |
| [List Indexes](actions/list-indexes.md) | GET | Retrieves indexes from Milvus Vector Store. |

### Partition

| Action | Method | Description |
| --- | --- | --- |
| [Create Partition](actions/create-partition.md) | POST | Creates a partition in Milvus Vector Store. |
| [Drop Partition](actions/drop-partition.md) | DELETE | Deletes a partition from Milvus Vector Store. |
| [Get Partition Statistics](actions/get-partition-statistics.md) | GET | Retrieves partition statistics from Milvus Vector Store. |
| [Has Partition](actions/has-partition.md) | GET | Checks whether a partition exists in Milvus Vector Store. |
| [List Partitions](actions/list-partitions.md) | GET | Retrieves partitions from Milvus Vector Store. |

### Vector Record

| Action | Method | Description |
| --- | --- | --- |
| [Delete Vectors](actions/delete-vectors.md) | DELETE | Deletes vectors from Milvus Vector Store. |
| [Get Vectors](actions/get-vectors.md) | GET | Retrieves vectors from Milvus Vector Store. |
| [Insert Vectors](actions/insert-vectors.md) | POST | Inserts vectors into Milvus Vector Store. |
| [Query Vectors](actions/query-vectors.md) | GET | Queries vectors in Milvus Vector Store. |
| [Upsert Vectors](actions/upsert-vectors.md) | PUT | Upserts vectors in Milvus Vector Store. |

### Vector Search

| Action | Method | Description |
| --- | --- | --- |
| [Hybrid Search Vectors](actions/hybrid-search-vectors.md) | GET | Runs a hybrid vector search in Milvus Vector Store. |
| [Search Vectors](actions/search-vectors.md) | GET | Searches vectors in Milvus Vector Store. |

