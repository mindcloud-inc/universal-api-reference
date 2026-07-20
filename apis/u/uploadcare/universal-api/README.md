# <img src="https://images.mindcloud.co/apps/icons/uploadcare-logo_1773930365397.png" alt="Uploadcare logo" width="28" height="28"> Uploadcare: Universal API

Upload, manage, convert, and deliver files

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uploadcare/latest
- **Category:** Content & Files / Storage
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://uploadcare.com/
- **Vendor API docs:** https://uploadcare.com/api-refs/rest-api/v0.7.0/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Files](actions/list-files.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Batch Delete Files](actions/batch-delete-files.md) | DELETE | Deletes multiple files from Uploadcare storage. |
| [Batch Store Files](actions/batch-store-files.md) | PUT | Stores multiple files in Uploadcare storage. |
| [Convert Document](actions/convert-document.md) | POST | Creates a document conversion in Uploadcare. |
| [Convert Video](actions/convert-video.md) | POST | Creates a video conversion in Uploadcare. |
| [Copy File To Local Storage](actions/copy-file-to-local-storage.md) | POST | Creates a local storage copy in Uploadcare. |
| [Delete File](actions/delete-file.md) | DELETE | Deletes an existing file from Uploadcare storage. |
| [Delete File Metadata Key](actions/delete-file-metadata-key.md) | DELETE | Deletes a file metadata key from Uploadcare. |
| [Get Document Conversion Info](actions/get-document-conversion-info.md) | GET | Retrieves document conversion info from Uploadcare. |
| [Get Document Conversion Status](actions/get-document-conversion-status.md) | GET | Retrieves document conversion status from Uploadcare by token. |
| [Get File](actions/get-file.md) | GET | Retrieves a file record from Uploadcare. |
| [Get File Metadata](actions/get-file-metadata.md) | GET | Retrieves all file metadata from Uploadcare. |
| [Get File Metadata Value](actions/get-file-metadata-value.md) | GET | Retrieves a file metadata value from Uploadcare by key. |
| [List Files](actions/list-files.md) | GET | Retrieves all files from your Uploadcare project. |
| [Store File](actions/store-file.md) | PUT | Stores an existing file in Uploadcare. |
| [Update File Metadata Value](actions/update-file-metadata-value.md) | PUT | Updates a file metadata value in Uploadcare. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from Uploadcare. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group record from Uploadcare. |
| [List Groups](actions/list-groups.md) | GET | Retrieves all groups from your Uploadcare project. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves current project details from Uploadcare. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Uploadcare. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from Uploadcare by target URL. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves all webhooks from your Uploadcare project. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Uploadcare. |

