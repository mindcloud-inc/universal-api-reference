# <img src="https://images.mindcloud.co/apps/icons/airparser_1773782077325.png" alt="Airparser logo" width="28" height="28"> Airparser: Universal API

Parse documents, extract structured data, and manage inbox schemas

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/airparser/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://airparser.com
- **Vendor API docs:** https://help.airparser.com/public-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Inboxes](actions/list-inboxes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airparser/latest/actions/list-inboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Extended Document Details](actions/get-extended-document-details.md) | GET | Retrieves extended document details from Airparser. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from an Airparser inbox. |
| [Parse Document Async](actions/parse-document-async.md) | POST | Parses a document asynchronously in Airparser. |
| [Parse Document Sync](actions/parse-document-sync.md) | POST | Parses a document synchronously in Airparser. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Clone Extraction Schema](actions/clone-extraction-schema.md) | POST | Clones an extraction schema between Airparser inboxes. |
| [Create Or Update Extraction Schema](actions/create-or-update-extraction-schema.md) | PUT | Creates or updates an extraction schema in Airparser. |
| [Delete Inbox](actions/delete-inbox.md) | DELETE | Deletes an existing inbox from Airparser. |
| [List Inboxes](actions/list-inboxes.md) | GET | Retrieves all inbox records from Airparser. |

