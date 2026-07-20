# List Deliveries with Mobile Text Alerts

Retrieves message deliveries from Mobile Text Alerts.

## Endpoint

- **Method:** `GET`
- **Path:** `/deliveries`
- **Base URL:** `https://api.mobile-text-alerts.com/v3`
- **Official documentation:** [List Deliveries](https://developers.mobile-text-alerts.com/api-reference/deliveries#get-deliveries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to retrieve. |
| `pageSize` | query | `number` | no | Number of results per page. |
| `query` | query | `string` | no | Search by subscriber name, number, or email. |
| `status` | query | `string` | no | Filter by delivery status. |
| `startDate` | query | `string` | no | Filter deliveries on or after YYYY-MM-DD. |
| `endDate` | query | `string` | no | Filter deliveries on or before YYYY-MM-DD. |
