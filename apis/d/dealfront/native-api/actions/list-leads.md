# List Leads with Dealfront

Retrieves leads from Dealfront.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/leads`
- **Base URL:** `https://api.leadfeeder.com`
- **Official documentation:** [List Leads](https://docs.leadfeeder.com/api/#get-leads)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | ID of the account whose leads you want to list. |
| `start_date` | query | `string` | yes | Start date for the lead search window in YYYY-MM-DD format. |
| `end_date` | query | `string` | yes | End date for the lead search window in YYYY-MM-DD format. |
