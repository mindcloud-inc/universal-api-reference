# <img src="https://images.mindcloud.co/apps/icons/restdbio-logo-official_1775841986573.png" alt="Restdb.io logo" width="28" height="28"> Restdb.io: Universal API

Connects Restdb.io database APIs so MindCloud can work with collections, documents, metadata, media, mail, and authentication endpoints in a Restdb.io tenant.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/restdbio/latest
- **Category:** IT Operations / Database
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://restdb.io/
- **Vendor API docs:** https://restdb.io/media/restdb-cheat-sheet.pdf

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Database Metadata](actions/get-database-metadata.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/get-database-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Generate JWT](actions/generate-jwt.md) | POST | Generates a JWT token in Restdb.io. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection Metadata](actions/get-collection-metadata.md) | GET | Retrieves collection metadata from Restdb.io. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Logout User](actions/logout-user.md) | DELETE | Logs out a Restdb.io user and invalidates the token. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET | Retrieves user information from Restdb.io. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [Get Database Metadata](actions/get-database-metadata.md) | GET | Retrieves database metadata from Restdb.io. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Aggregate Documents](actions/aggregate-documents.md) | GET | Retrieves aggregated document results from Restdb.io. |
| [Bulk Create Documents](actions/bulk-create-documents.md) | POST | Creates multiple documents in Restdb.io. |
| [Bulk Delete Documents](actions/bulk-delete-documents.md) | DELETE | Deletes multiple documents from Restdb.io by ID list. |
| [Count Documents](actions/count-documents.md) | GET | Retrieves document counts from a Restdb.io collection. |
| [Create Child Document](actions/create-child-document.md) | POST | Creates a child document in Restdb.io. |
| [Create Document](actions/create-document.md) | POST | Creates a new document in Restdb.io. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a document from Restdb.io. |
| [Delete Documents By Query](actions/delete-documents-by-query.md) | DELETE | Deletes documents from Restdb.io by query. |
| [Get Child Document](actions/get-child-document.md) | GET | Retrieves a child document from Restdb.io by ID. |
| [Get Child Documents](actions/get-child-documents.md) | GET | Retrieves child documents from a Restdb.io record. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Restdb.io by ID. |
| [Get Document References](actions/get-document-references.md) | GET | Retrieves records that reference a Restdb.io document. |
| [Group Documents](actions/group-documents.md) | GET | Retrieves documents grouped by a Restdb.io field. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from a Restdb.io collection. |
| [List Documents Flattened](actions/list-documents-flattened.md) | GET | Retrieves flattened reference URL fields from Restdb.io documents. |
| [List Documents With Children](actions/list-documents-with-children.md) | GET | Retrieves documents with child records from Restdb.io. |
| [List Documents With Linked References](actions/list-documents-with-linked-references.md) | GET | Retrieves documents with canonical reference URLs from Restdb.io. |
| [List Documents With Media Data](actions/list-documents-with-media-data.md) | GET | Retrieves documents with media records from Restdb.io. |
| [List Documents With Meta Fields](actions/list-documents-with-meta-fields.md) | GET | Retrieves documents with internal meta fields from Restdb.io. |
| [List Documents With Totals](actions/list-documents-with-totals.md) | GET | Retrieves documents and totals from a Restdb.io collection. |
| [Patch Document](actions/patch-document.md) | PUT | Updates selected fields on a Restdb.io document. |
| [Replace Document](actions/replace-document.md) | PUT | Replaces an existing document in Restdb.io. |
| [Search Documents](actions/search-documents.md) | GET | Finds documents in Restdb.io by text search. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Send Email](actions/send-email.md) | POST | Sends an email through Restdb.io. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete Media](actions/delete-media.md) | DELETE | Deletes media content from Restdb.io. |
| [Get Media Metadata](actions/get-media-metadata.md) | GET | Retrieves media metadata from Restdb.io. |
| [Upload Media](actions/upload-media.md) | POST | Uploads media files to Restdb.io. |

