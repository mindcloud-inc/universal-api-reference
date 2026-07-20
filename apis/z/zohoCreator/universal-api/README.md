# <img src="https://images.mindcloud.co/apps/icons/zoho-creator-header_1775222648150.png" alt="Zoho Creator logo" width="28" height="28"> Zoho Creator: Universal API

Create apps and manage forms, data, and workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoCreator/latest
- **Category:** IT Operations / Database
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/creator/
- **Vendor API docs:** https://www.zoho.com/creator/help/api/v2.1/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Applications](actions/get-applications.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/get-applications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Get Applications](actions/get-applications.md) | GET | Retrieves accessible applications from Zoho Creator. |
| [Get Applications by Workspace](actions/get-applications-by-workspace.md) | GET | Retrieves workspace applications from Zoho Creator. |

### Bulk Read Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Bulk Read Job](actions/create-bulk-read-job.md) | POST | Creates a bulk read job in Zoho Creator. |
| [Get Bulk Read Job Status](actions/get-bulk-read-job-status.md) | GET | Retrieves the status of a Zoho Creator bulk read job. |

### Bulk Read Result

| Action | Method | Description |
| --- | --- | --- |
| [Download Bulk Read Result](actions/download-bulk-read-result.md) | GET | Downloads the result of a Zoho Creator bulk read job. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Fields](actions/get-fields.md) | GET | Retrieves fields from a Zoho Creator form. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET | Retrieves a file from a Zoho Creator record. |
| [Download File from Subform](actions/download-file-from-subform.md) | GET | Retrieves a file from a Zoho Creator subform record. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to a Zoho Creator record. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Forms](actions/get-forms.md) | GET | Retrieves forms from a Zoho Creator application. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Pages](actions/get-pages.md) | GET | Retrieves pages from a Zoho Creator application. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Add Records](actions/add-records.md) | POST | Creates new records in a Zoho Creator form. |
| [Delete Record by ID](actions/delete-record-by-id.md) | DELETE | Deletes a specific Zoho Creator record by ID. |
| [Delete Records](actions/delete-records.md) | DELETE | Deletes records from a Zoho Creator report. |
| [Get Record by ID](actions/get-record-by-id.md) | GET | Retrieves a specific Zoho Creator record by ID. |
| [Get Records](actions/get-records.md) | GET | Retrieves records from a Zoho Creator report. |
| [Publish Add Records](actions/publish-add-records.md) | POST | Creates new records through a Zoho Creator publish form. |
| [Publish Get Record by ID](actions/publish-get-record-by-id.md) | GET | Retrieves a specific published Zoho Creator record by ID. |
| [Publish Get Records](actions/publish-get-records.md) | GET | Retrieves published records from a Zoho Creator report. |
| [Update Record by ID](actions/update-record-by-id.md) | PUT | Updates a specific Zoho Creator record by ID. |
| [Update Records](actions/update-records.md) | PUT | Updates records in a Zoho Creator report. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Reports](actions/get-reports.md) | GET | Retrieves reports from a Zoho Creator application. |

### Section

| Action | Method | Description |
| --- | --- | --- |
| [Get Sections](actions/get-sections.md) | GET | Retrieves sections from a Zoho Creator application. |

