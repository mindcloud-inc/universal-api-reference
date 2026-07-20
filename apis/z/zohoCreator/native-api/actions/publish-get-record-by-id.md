# Publish Get Record by ID with Zoho Creator

Retrieves a specific published Zoho Creator record by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/publish/:account_owner_name/:app_link_name/report/:report_link_name/:record_ID`
- **Base URL:** `https://www.zohoapis.com/creator/v2.1`
- **Official documentation:** [Publish Get Record by ID](https://www.zoho.com/creator/help/api/v2.1/publish-api/get-record-by-id.html)

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
| `field_config` | query | `string` | no | Response field configuration mode. |
| `fields[]` | query | `array<string>` | no | Fields to include in the response. |
| `privatelink` | query | `string` | yes | Zoho Creator publish API private link token. |
| `record_ID` | path | `string` | yes | Zoho Creator record ID. |
| `report_link_name` | path | `string` | yes | Zoho Creator report link name. |
