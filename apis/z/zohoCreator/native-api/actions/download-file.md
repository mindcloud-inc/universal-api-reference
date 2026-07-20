# Download File with Zoho Creator

Retrieves a file from a Zoho Creator record.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/:account_owner_name/:app_link_name/report/:report_link_name/:record_ID/:field_link_name/download`
- **Base URL:** `https://www.zohoapis.com/creator/v2.1`
- **Official documentation:** [Download File](https://www.zoho.com/creator/help/api/v2.1/download-file.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_owner_name` | path | `string` | yes | Zoho Creator account owner name. |
| `app_link_name` | path | `string` | yes | Zoho Creator app link name. |
| `field_link_name` | path | `string` | yes | Zoho Creator field link name for the file field. |
| `record_ID` | path | `string` | yes | Zoho Creator record ID. |
| `report_link_name` | path | `string` | yes | Zoho Creator report link name. |
