# <img src="https://images.mindcloud.co/apps/icons/flatfile-icon-512_1775826588725.png" alt="Flatfile logo" width="28" height="28"> Flatfile: Universal API

Flatfile API integration for managing environments, spaces, workbooks, sheets, records, files, jobs, users, views, documents, snapshots, and data clips.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/flatfile/latest
- **Actions:** 51
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://flatfile.com
- **Vendor API docs:** https://reference.flatfile.com/overview/welcome

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Environments](actions/list-environments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/list-environments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (51)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Account](actions/get-current-account.md) | GET | Retrieves the current account from Flatfile. |

### Calculation

| Action | Method | Description |
| --- | --- | --- |
| [List Calculations](actions/list-calculations.md) | GET | Retrieves calculations for a sheet in Flatfile. |

### Cell Value

| Action | Method | Description |
| --- | --- | --- |
| [Get Cell Values](actions/get-cell-values.md) | GET | Retrieves record cell values by field in Flatfile. |

### Environment

| Action | Method | Description |
| --- | --- | --- |
| [Get Environment](actions/get-environment.md) | GET | Retrieves a specific environment from Flatfile. |
| [List Environments](actions/list-environments.md) | GET | Retrieves a list of environments from Flatfile. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Clone File](actions/clone-file.md) | POST | Creates a copy of a file in Flatfile. |
| [Delete File](actions/delete-file.md) | DELETE | Deletes an existing file from Flatfile. |
| [Get File](actions/get-file.md) | GET | Retrieves a specific file from Flatfile. |
| [List Files](actions/list-files.md) | GET | Retrieves a list of files from Flatfile. |
| [Update File](actions/update-file.md) | PUT | Updates an existing file in Flatfile. |
| [Upload File](actions/upload-file.md) | POST | Uploads a new file to Flatfile. |

### File Download

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET | Downloads a specific file from Flatfile. |

### Header Detection

| Action | Method | Description |
| --- | --- | --- |
| [Detect File Header](actions/detect-file-header.md) | POST | Detects the header row in a Flatfile file. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Acknowledge Job](actions/acknowledge-job.md) | PUT | Acknowledges a specific job in Flatfile. |
| [Complete Job](actions/complete-job.md) | PUT | Completes a specific job in Flatfile. |
| [Create Job](actions/create-job.md) | POST | Creates a new job in Flatfile. |
| [Delete Job](actions/delete-job.md) | DELETE | Deletes an existing job from Flatfile. |
| [Execute Job](actions/execute-job.md) | PUT | Executes a specific job in Flatfile. |
| [Get Job](actions/get-job.md) | GET | Retrieves a specific job from Flatfile. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves a list of jobs from Flatfile. |
| [Update Job](actions/update-job.md) | PUT | Updates an existing job in Flatfile. |

### Job Execution Plan

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Execution Plan](actions/get-job-execution-plan.md) | GET | Retrieves a job execution plan from Flatfile. |

### Publishable Key

| Action | Method | Description |
| --- | --- | --- |
| [Get Publishable Key](actions/get-publishable-key.md) | GET | Retrieves a publishable key for a Flatfile environment. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Records](actions/bulk-update-records.md) | PUT | Bulk updates matching records in a Flatfile sheet. |
| [Delete Records](actions/delete-records.md) | DELETE | Deletes records from a Flatfile sheet. |
| [Find And Replace Records](actions/find-and-replace-records.md) | PUT | Finds and replaces matching record values in Flatfile. |
| [Get Records](actions/get-records.md) | GET | Retrieves records from a sheet in Flatfile. |
| [Insert Records](actions/insert-records.md) | POST | Creates new records in a Flatfile sheet. |
| [Update Records](actions/update-records.md) | PUT | Updates existing records in a Flatfile sheet. |

### Record Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Record Counts](actions/get-record-counts.md) | GET | Retrieves record counts for a Flatfile sheet. |

### Record Index

| Action | Method | Description |
| --- | --- | --- |
| [Get Record Indices](actions/get-record-indices.md) | GET | Retrieves record indices from a Flatfile sheet. |

### Sheet

| Action | Method | Description |
| --- | --- | --- |
| [Delete Sheet](actions/delete-sheet.md) | DELETE | Deletes an existing sheet from Flatfile. |
| [Duplicate Sheet](actions/duplicate-sheet.md) | POST | Creates a duplicate of a sheet in Flatfile. |
| [Get Sheet](actions/get-sheet.md) | GET | Retrieves a specific sheet from Flatfile. |
| [List Sheets](actions/list-sheets.md) | GET | Retrieves a list of sheets from Flatfile. |
| [Update Sheet](actions/update-sheet.md) | PUT | Updates an existing sheet in Flatfile. |

### Sheet Commit

| Action | Method | Description |
| --- | --- | --- |
| [Get Sheet Commits](actions/get-sheet-commits.md) | GET | Retrieves commit versions for a sheet in Flatfile. |

### Sheet Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Sheet](actions/validate-sheet.md) | PUT | Runs validation on a sheet in Flatfile. |

### Space

| Action | Method | Description |
| --- | --- | --- |
| [Archive Space](actions/archive-space.md) | PUT | Archives an existing space in Flatfile. |
| [Create Space](actions/create-space.md) | POST | Creates a new space in Flatfile. |
| [Delete Space](actions/delete-space.md) | DELETE | Deletes an existing space from Flatfile. |
| [Get Space](actions/get-space.md) | GET | Retrieves a specific space from Flatfile. |
| [List Spaces](actions/list-spaces.md) | GET | Retrieves a list of spaces from Flatfile. |
| [Unarchive Space](actions/unarchive-space.md) | PUT | Unarchives an existing space in Flatfile. |
| [Update Space](actions/update-space.md) | PUT | Updates an existing space in Flatfile. |

### Workbook

| Action | Method | Description |
| --- | --- | --- |
| [Create Workbook](actions/create-workbook.md) | POST | Creates a new workbook in Flatfile. |
| [Delete Workbook](actions/delete-workbook.md) | DELETE | Deletes an existing workbook from Flatfile. |
| [Get Workbook](actions/get-workbook.md) | GET | Retrieves a specific workbook from Flatfile. |
| [List Workbooks](actions/list-workbooks.md) | GET | Retrieves a list of workbooks from Flatfile. |
| [Update Workbook](actions/update-workbook.md) | PUT | Updates an existing workbook in Flatfile. |

### Workbook Commit

| Action | Method | Description |
| --- | --- | --- |
| [Get Workbook Commits](actions/get-workbook-commits.md) | GET | Retrieves commits for a workbook in Flatfile. |

