# Publish Get Records with Zoho Creator

Retrieves published records from a Zoho Creator report.

## Endpoint

- **Method:** `GET`
- **Path:** `/publish/:account_owner_name/:app_link_name/report/:report_link_name`
- **Base URL:** `https://www.zohoapis.com/creator/v2.1`
- **Official documentation:** [Publish Get Records](https://www.zoho.com/creator/help/api/v2.1/publish-api/get-records.html)

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
| `criteria` | query | `string` | no | Zoho Creator criteria expression used to filter records. |
| `field_config` | query | `string` | no | Response field configuration mode. |
| `fields[]` | query | `array<string>` | no | Fields to include in the response. |
| `from` | query | `number` | no | Starting record offset. |
| `limit` | query | `number` | no | Maximum number of records to return. |
| `max_records` | query | `number` | no | Upper bound on records returned by the query. |
| `privatelink` | query | `string` | yes | Zoho Creator publish API private link token. |
| `report_link_name` | path | `string` | yes | Zoho Creator report link name. |
