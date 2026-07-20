# Get Organization Sales Report with Eventbrite

Retrieves an organization sales report from Eventbrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/reports/sales/`
- **Base URL:** `https://www.eventbriteapi.com/v3`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | query | `string` | yes | End datetime in UTC ISO format. |
| `event_ids` | query | `string` | yes | One or more Eventbrite event IDs. |
| `organizationId` | path | `string` | yes | Organization identifier. |
| `start_date` | query | `string` | yes | Start datetime in UTC ISO format. |
