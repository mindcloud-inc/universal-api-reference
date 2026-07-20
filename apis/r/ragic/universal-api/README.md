# <img src="https://images.mindcloud.co/apps/icons/ragic_1773777790065.png" alt="Ragic logo" width="28" height="28"> Ragic: Universal API

Build databases, manage forms, and automate business workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ragic/latest
- **Category:** IT Operations / Database
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ragic.com/
- **Vendor API docs:** https://www.ragic.com/docs/api/en/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Records](actions/list-records.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ragic/latest/actions/list-records?connectionId=$CONNECTION_ID&limit=25&offset=0&tabFolderPath=ragic-setup&sheetIndex=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Action Button

| Action | Method | Description |
| --- | --- | --- |
| [Execute Action Button](actions/execute-action-button.md) | PUT | Executes an action button on a Ragic record. |
| [List Action Buttons](actions/list-action-buttons.md) | GET | Retrieves action buttons from Ragic. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Add Record Comment](actions/add-record-comment.md) | PUT | Adds a comment to a record in Ragic. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get Attachment / File](actions/get-attachment-file.md) | GET | Retrieves an attachment or file from Ragic. |

### Mass Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Mass Task Status](actions/get-mass-task-status.md) | GET | Retrieves mass task status from Ragic. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | POST | Creates a new record in Ragic. |
| [Delete Record](actions/delete-record.md) | DELETE | Deletes an existing record from Ragic. |
| [Get Custom Print Report](actions/get-custom-print-report.md) | GET | Retrieves a custom print report from Ragic. |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from Ragic. |
| [Get Record As Excel](actions/get-record-as-excel.md) | GET | Retrieves a record as Excel from Ragic. |
| [Get Record As HTML](actions/get-record-as-html.md) | GET | Retrieves a record as HTML from Ragic. |
| [Get Record As PDF](actions/get-record-as-pdf.md) | GET | Retrieves a record as PDF from Ragic. |
| [Import From URL](actions/import-from-url.md) | POST | Imports records into Ragic from a URL. |
| [List Records](actions/list-records.md) | GET | Retrieves records from Ragic. |
| [Lock Record](actions/lock-record.md) | PUT | Locks a record in Ragic. |
| [Mass Approve Records](actions/mass-approve-records.md) | PUT | Approves multiple records in Ragic. |
| [Mass Execute Action Button](actions/mass-execute-action-button.md) | PUT | Executes an action button on multiple Ragic records. |
| [Mass Lock Records](actions/mass-lock-records.md) | PUT | Locks multiple records in Ragic. |
| [Mass Reject Records](actions/mass-reject-records.md) | PUT | Rejects multiple records in Ragic. |
| [Mass Search And Replace](actions/mass-search-and-replace.md) | PUT | Replaces matching values across multiple Ragic records. |
| [Mass Unlock Records](actions/mass-unlock-records.md) | PUT | Unlocks multiple records in Ragic. |
| [Mass Update Records](actions/mass-update-records.md) | PUT | Updates multiple records in Ragic. |
| [Patch Record](actions/patch-record.md) | PUT | Partially updates an existing record in Ragic. |
| [Replace Record](actions/replace-record.md) | PUT | Replaces an existing record in Ragic. |
| [Unlock Record](actions/unlock-record.md) | PUT | Unlocks a record in Ragic. |
| [Update Record](actions/update-record.md) | PUT | Updates an existing record in Ragic. |
| [Upload Files and Images](actions/upload-files-and-images.md) | POST | Uploads files and images to Ragic. |

### Webhook Public Key

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook Public Key As PEM](actions/get-webhook-public-key-as-pem.md) | GET | Retrieves the Ragic webhook public key as PEM. |
| [Get Webhook Public Key As String](actions/get-webhook-public-key-as-string.md) | GET | Retrieves the Ragic webhook public key as a string. |

