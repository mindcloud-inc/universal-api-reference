# List Templates with Docupilot

Retrieves templates from Docupilot.

## Endpoint

- **Method:** `GET`
- **Path:** `/dashboard/api/v2/templates/`
- **Base URL:** `https://api.docupilot.app`
- **Official documentation:** [List Templates](https://help.docupilot.app/developers/templates-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `delivery_type` | query | `list<string>` | no | Filter templates by configured delivery type (supports multiple values) Accepted values: `aws_s3`, `azure_blob_storage`, `box_drive`, `docu_sign`, `dropbox`, `email`, `eversign`, `google_drive`, `hellosign`, `one_drive`, `podio`, `sftp`, `sign_now`, `signable`, `signature`, `webhook`, `yousign`, `zoho_crm`. Send multiple values as a array. |
| `folder` | query | `number` | no | — |
| `ordering` | query | `string` | no | Which field to use when ordering the results. |
| `output_type` | query | `list` | no | Accepted values: `docx`, `html`, `jpeg`, `pdf`, `png`, `pptx`, `xlsx`. |
| `page` | query | `number` | no | A page number within the paginated result set. |
| `search` | query | `string` | no | Search templates by title |
| `status` | query | `list` | no | Filter templates by status (all, active, test) Accepted values: `active`, `test`. |
| `type` | query | `list` | no | Accepted values: `docx`, `fillable_pdf`, `g_document`, `g_presentation`, `g_spreadsheet`, `html`, `pptx`, `xlsx`. |
