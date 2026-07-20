# <img src="https://images.mindcloud.co/apps/icons/needle_1775752353473.png" alt="Needle logo" width="28" height="28"> Needle: Universal API

Create, search, and manage Needle collections and files

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/needle/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://needle.app
- **Vendor API docs:** https://docs.needle.app/docs/api-reference/needle-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get File Upload URL](actions/get-file-upload-url.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/needle/latest/actions/get-file-upload-url?connectionId=$CONNECTION_ID&contentType=application%2Fpdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in Needle. |
| [Get Collection Details](actions/get-collection-details.md) | GET | Retrieves details for a collection from Needle. |
| [Get Collection Stats](actions/get-collection-stats.md) | GET | Retrieves statistics for a collection from Needle. |
| [List Collections](actions/list-collections.md) | GET | Retrieves all collections from Needle. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Add Files To Collection](actions/add-files-to-collection.md) | POST | Adds files to a collection in Needle. |
| [Delete Files From Collection](actions/delete-files-from-collection.md) | DELETE | Deletes files from a collection in Needle. |
| [Get File Download URL](actions/get-file-download-url.md) | GET | Retrieves a signed file download URL from Needle. |
| [Get File Upload URL](actions/get-file-upload-url.md) | GET | Retrieves a signed file upload URL from Needle. |
| [List Collection Files](actions/list-collection-files.md) | GET | Retrieves files from a Needle collection. |
| [Search Collection](actions/search-collection.md) | GET | Searches a collection in Needle by query. |

