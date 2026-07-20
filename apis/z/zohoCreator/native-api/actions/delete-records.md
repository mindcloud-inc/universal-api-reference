# Delete Records with Zoho Creator

Deletes records from a Zoho Creator report.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/data/:account_owner_name/:app_link_name/report/:report_link_name`
- **Base URL:** `https://www.zohoapis.com/creator/v2.1`
- **Official documentation:** [Delete Records](https://www.zoho.com/creator/help/api/v2.1/delete-records.html)

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
| `criteria` | body | `string` | yes | Criteria used to select records for deletion. |
| `process_until_limit` | query | `boolean` | no | Continue processing until the limit is reached. |
| `report_link_name` | path | `string` | yes | Zoho Creator report link name. |
| `result` | body | `object` | no | Response result preferences. |
| `skip_workflow[]` | body | `array<string>` | no | Workflows to skip during the deletion. |
