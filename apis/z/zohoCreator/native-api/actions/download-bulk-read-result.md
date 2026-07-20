# Download Bulk Read Result with Zoho Creator

Downloads the result of a Zoho Creator bulk read job.

## Endpoint

- **Method:** `GET`
- **Path:** `/bulk/:account_owner_name/:app_link_name/report/:report_link_name/read/:job_ID/result`
- **Base URL:** `https://www.zohoapis.com/creator/v2.1`
- **Official documentation:** [Download Bulk Read Result](https://www.zoho.com/creator/help/api/v2.1/bulk-api/download-bulk-read-result.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_owner_name` | path | `string` | yes | Zoho Creator account owner name. |
| `app_link_name` | path | `string` | yes | Zoho Creator app link name. |
| `job_ID` | path | `string` | yes | Zoho Creator bulk read job ID. |
| `report_link_name` | path | `string` | yes | Zoho Creator report link name. |
