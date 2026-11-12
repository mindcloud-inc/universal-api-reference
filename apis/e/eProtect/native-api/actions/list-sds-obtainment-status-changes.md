# List SDS Obtainment Status Changes with 3E Protect

## Endpoint

- **Method:** `GET`
- **Path:** `/catalog-item-obtainment-status`
- **Base URL:** `{apiBaseUrl}`
- **API:** rest
- **Official documentation:** [List SDS Obtainment Status Changes](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item-obtainment-status/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | query | `string` | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
| `startDate` | query | `date` | yes | Include status changes since this date. Sent as YYYY-MM-DD. |
| `endDate` | query | `date` | no | Optional end of the status-change date range. Sent as YYYY-MM-DD. |
