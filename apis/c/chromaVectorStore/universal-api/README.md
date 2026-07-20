# <img src="https://images.mindcloud.co/apps/icons/chroma-vector-store_1775857142401.png" alt="Chroma Vector Store logo" width="28" height="28"> Chroma Vector Store: Universal API

Chroma Cloud vector database for managing tenants, databases, collections, and vector records for AI retrieval workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chromaVectorStore/latest
- **Category:** IT Operations / Database
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.trychroma.com
- **Vendor API docs:** https://docs.trychroma.com/reference/chroma-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Identity](actions/get-user-identity.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chromaVectorStore/latest/actions/get-user-identity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in Chroma. |
| [Fork Collection](actions/fork-collection.md) | POST | Creates a fork of an existing collection in Chroma. |
| [Get Records](actions/get-records.md) | GET | Retrieves collection records from Chroma by ID or metadata filter. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [Create Database](actions/create-database.md) | POST | Creates a new database in Chroma. |
| [List Databases](actions/list-databases.md) | GET | Retrieves tenant database records from Chroma. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [List Sources](actions/list-sources.md) | GET | Retrieves tenant source records from Chroma. |

### System

| Action | Method | Description |
| --- | --- | --- |
| [Heartbeat](actions/heartbeat.md) | GET | Retrieves the current nanosecond timestamp from Chroma. |

### Tenant

| Action | Method | Description |
| --- | --- | --- |
| [Create Tenant](actions/create-tenant.md) | POST | Creates a new tenant in Chroma. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Identity](actions/get-user-identity.md) | GET | Retrieves user identity details from Chroma. |

