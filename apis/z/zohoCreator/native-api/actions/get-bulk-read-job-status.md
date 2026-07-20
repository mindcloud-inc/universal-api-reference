# Get Bulk Read Job Status with Zoho Creator

Retrieves the status of a Zoho Creator bulk read job.

## Endpoint

- **Method:** `GET`
- **Path:** `/bulk/:account_owner_name/:app_link_name/report/:report_link_name/read/:job_ID`
- **Base URL:** `https://www.zohoapis.com/creator/v2.1`
- **Official documentation:** [Get Bulk Read Job Status](https://www.zoho.com/creator/help/api/v2.1/bulk-api/get-the-status-of-the-bulk-read-job.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_owner_name` | path | `string` | yes | Zoho Creator account owner name. |
| `app_link_name` | path | `string` | yes | Zoho Creator app link name. |
| `job_ID` | path | `string` | yes | Zoho Creator bulk read job ID. |
| `report_link_name` | path | `string` | yes | Zoho Creator report link name. |
