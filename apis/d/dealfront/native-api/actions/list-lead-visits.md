# List Lead Visits with Dealfront

Retrieves visits for a lead in Dealfront.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/leads/:lead_id/visits`
- **Base URL:** `https://api.leadfeeder.com`
- **Official documentation:** [List Lead Visits](https://docs.leadfeeder.com/api/#get-all-visits-of-a-lead)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | ID of the account that owns the lead visit data. |
| `lead_id` | path | `string` | yes | ID of the lead whose visits you want to list. |
| `start_date` | query | `string` | yes | Start date for the visit search window in YYYY-MM-DD format. |
| `end_date` | query | `string` | yes | End date for the visit search window in YYYY-MM-DD format. |
