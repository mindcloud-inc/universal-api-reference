# Download File from Subform with Zoho Creator

Retrieves a file from a Zoho Creator subform record.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/:account_owner_name/:app_link_name/report/:report_link_name/:record_ID/:subform_link_name/:field_link_name/:subform_record_ID/download`
- **Base URL:** `https://www.zohoapis.com/creator/v2.1`
- **Official documentation:** [Download File from Subform](https://www.zoho.com/creator/help/api/v2.1/download-file-from-subform.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_owner_name` | path | `string` | yes | Zoho Creator account owner name. |
| `app_link_name` | path | `string` | yes | Zoho Creator app link name. |
| `field_link_name` | path | `string` | yes | Zoho Creator field link name for the file field. |
| `record_ID` | path | `string` | yes | Zoho Creator record ID. |
| `report_link_name` | path | `string` | yes | Zoho Creator report link name. |
| `subform_link_name` | path | `string` | yes | Zoho Creator subform link name. |
| `subform_record_ID` | path | `string` | yes | Zoho Creator subform record ID. |
