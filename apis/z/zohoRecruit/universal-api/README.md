# <img src="https://images.mindcloud.co/apps/icons/recruit-512_1775165679902.png" alt="Zoho Recruit logo" width="28" height="28"> Zoho Recruit: Universal API

Manage candidates, job records, users, and recruiting data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoRecruit/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/recruit/
- **Vendor API docs:** https://www.zoho.com/recruit/developer-guide/apiv2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Modules](actions/list-modules.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/list-modules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Delete Attachment](actions/delete-attachment.md) | DELETE | Deletes an attachment from a Zoho Recruit record. |
| [Download Attachment](actions/download-attachment.md) | GET | Retrieves an attachment from a Zoho Recruit record. |
| [Upload Attachment](actions/upload-attachment.md) | POST | Uploads an attachment to a Zoho Recruit record. |

### Bulk Read Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Bulk Read Job Details](actions/get-bulk-read-job-details.md) | GET | Retrieves bulk read job details from Zoho Recruit. |
| [Initiate Bulk Read Job](actions/initiate-bulk-read-job.md) | GET | Initiates a bulk read job in Zoho Recruit. |

### Bulk Read Result

| Action | Method | Description |
| --- | --- | --- |
| [Download Bulk Read Result](actions/download-bulk-read-result.md) | GET | Downloads a bulk read result from Zoho Recruit. |

### Custom View

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Views](actions/list-custom-views.md) | GET | Retrieves custom views from Zoho Recruit. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [List Fields](actions/list-fields.md) | GET | Retrieves field metadata from Zoho Recruit. |

### Module

| Action | Method | Description |
| --- | --- | --- |
| [Get Module](actions/get-module.md) | GET | Retrieves a module from Zoho Recruit. |
| [List Modules](actions/list-modules.md) | GET | Retrieves all modules from Zoho Recruit. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Notes](actions/create-notes.md) | POST | Creates new notes in Zoho Recruit. |
| [Delete Note](actions/delete-note.md) | DELETE | Deletes a note from Zoho Recruit. |
| [List Notes](actions/list-notes.md) | GET | Retrieves all notes from Zoho Recruit. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Records](actions/create-records.md) | POST | Creates new records in a Zoho Recruit module. |
| [Delete Records](actions/delete-records.md) | DELETE | Deletes records from a Zoho Recruit module. |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from a Zoho Recruit module. |
| [List Records](actions/list-records.md) | GET | Retrieves records from a Zoho Recruit module. |
| [Search Records](actions/search-records.md) | GET | Finds records in Zoho Recruit by search criteria. |
| [Update Records](actions/update-records.md) | PUT | Updates records in a Zoho Recruit module. |
| [Upsert Records](actions/upsert-records.md) | POST | Inserts or updates records in a Zoho Recruit module. |

### Related Record

| Action | Method | Description |
| --- | --- | --- |
| [Get Related Records](actions/get-related-records.md) | GET | Retrieves related records from Zoho Recruit. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Add Tags](actions/add-tags.md) | PUT | Adds tags to a Zoho Recruit record. |
| [Remove Tags](actions/remove-tags.md) | PUT | Removes tags from a Zoho Recruit record. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves all users from Zoho Recruit. |

