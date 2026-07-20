# Create Bulk Read Job with Zoho Creator

Creates a bulk read job in Zoho Creator.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk/:account_owner_name/:app_link_name/report/:report_link_name/read`
- **Base URL:** `https://www.zohoapis.com/creator/v2.1`
- **Official documentation:** [Create Bulk Read Job](https://www.zoho.com/creator/help/api/v2.1/bulk-api/create-bulk-read-job.html)

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
| `query` | body | `object` | yes | Bulk read query options including criteria, fields, and maxRecords. |
| `report_link_name` | path | `string` | yes | Zoho Creator report link name. |
