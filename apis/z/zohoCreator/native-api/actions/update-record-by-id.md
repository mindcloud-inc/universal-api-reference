# Update Record by ID with Zoho Creator

Updates a specific Zoho Creator record by ID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/data/:account_owner_name/:app_link_name/report/:report_link_name/:record_ID`
- **Base URL:** `https://www.zohoapis.com/creator/v2.1`
- **Official documentation:** [Update Record by ID](https://www.zoho.com/creator/help/api/v2.1/update-specific-record.html)

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
| `data` | body | `object` | yes | Field values to update on the selected record. |
| `record_ID` | path | `string` | yes | Zoho Creator record ID. |
| `report_link_name` | path | `string` | yes | Zoho Creator report link name. |
| `result` | body | `object` | no | Response result preferences. |
| `skip_workflow[]` | body | `array<string>` | no | Workflows to skip during the update. |
