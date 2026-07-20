# List Visiting Companies with Salespanel

Retrieves visiting companies from your Salespanel account.

## Endpoint

- **Method:** `GET`
- **Path:** `/visiting-companies/`
- **Base URL:** `https://salespanel.io/api/v1`
- **Official documentation:** [List Visiting Companies](https://salespanel.io/docs/#get-all-visiting-companies)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `select_by_first_activity` | query | `boolean` | no | Retrieve visiting companies based on first activity instead of most recent activity. |
