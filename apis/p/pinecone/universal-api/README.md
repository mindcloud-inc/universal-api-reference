# <img src="https://images.mindcloud.co/apps/icons/icon-1_1774300624034.png" alt="Pinecone logo" width="28" height="28"> Pinecone: Universal API

Store, search, and manage vector indexes

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pinecone/latest
- **Category:** IT Operations / Database
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pinecone.io
- **Vendor API docs:** https://docs.pinecone.io/reference/api/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Describe Backup](actions/describe-backup.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/describe-backup?connectionId=$CONNECTION_ID&backupId=bbe4c309-c63e-4770-8550-b18ee77b87bd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Backup

| Action | Method | Description |
| --- | --- | --- |
| [List Index Backups](actions/list-index-backups.md) | GET | Retrieves backups for a Pinecone index. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [List Collections](actions/list-collections.md) | GET | Retrieves collections for a Pinecone project. |

### Import

| Action | Method | Description |
| --- | --- | --- |
| [List Imports](actions/list-imports.md) | GET | Retrieves imports from a Pinecone index. |

### Index

| Action | Method | Description |
| --- | --- | --- |
| [Configure Index](actions/configure-index.md) | PUT | Updates an existing index in Pinecone. |
| [Create Index](actions/create-index.md) | POST | Creates a new index in Pinecone. |
| [Create Index With Integrated Embedding](actions/create-index-with-integrated-embedding.md) | POST | Creates an index with integrated embedding in Pinecone. |
| [Describe Index](actions/describe-index.md) | GET | Retrieves details for an index from Pinecone. |
| [Get Index Stats](actions/get-index-stats.md) | GET | Retrieves statistics for a Pinecone index. |
| [List Indexes](actions/list-indexes.md) | GET | Retrieves indexes for a Pinecone project. |

### Namespace

| Action | Method | Description |
| --- | --- | --- |
| [Create Namespace](actions/create-namespace.md) | POST | Creates a namespace in a Pinecone index. |
| [Delete Namespace](actions/delete-namespace.md) | DELETE | Deletes a namespace from a Pinecone index. |
| [Describe Namespace](actions/describe-namespace.md) | GET | Retrieves details for a namespace from Pinecone. |
| [List Namespaces](actions/list-namespaces.md) | GET | Retrieves namespaces from a Pinecone index. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Backup](actions/create-backup.md) | POST | Creates a backup for a Pinecone index. |
| [Create Index From Backup](actions/create-index-from-backup.md) | POST | Creates a Pinecone index from a backup. |
| [Delete Backup](actions/delete-backup.md) | DELETE | Deletes a backup from Pinecone. |
| [Describe Backup](actions/describe-backup.md) | GET | Retrieves details for a backup from Pinecone. |
| [Describe Model](actions/describe-model.md) | GET | Retrieves details for a Pinecone model. |
| [Describe Restore Job](actions/describe-restore-job.md) | GET | Retrieves details for a restore job from Pinecone. |
| [Generate Vectors](actions/generate-vectors.md) | POST | Generates vectors from input data in Pinecone. |
| [List Models](actions/list-models.md) | GET | Retrieves available inference models from Pinecone. |
| [List Project Backups](actions/list-project-backups.md) | GET | Retrieves backups for all indexes in Pinecone. |
| [List Restore Jobs](actions/list-restore-jobs.md) | GET | Retrieves restore jobs for Pinecone backups. |
| [Rerank Results](actions/rerank-results.md) | POST | Reranks search results with a Pinecone model. |

