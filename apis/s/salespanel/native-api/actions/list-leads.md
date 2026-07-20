# List Leads with Salespanel

Retrieves leads from your Salespanel account.

## Endpoint

- **Method:** `GET`
- **Path:** `/leads/`
- **Base URL:** `https://salespanel.io/api/v1`
- **Official documentation:** [List Leads](https://salespanel.io/docs/#get-all-leads)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `select_by_first_activity` | query | `boolean` | no | Retrieve leads based on first activity instead of most recent activity. |
