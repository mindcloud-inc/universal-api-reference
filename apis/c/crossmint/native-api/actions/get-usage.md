# Get Usage with Crossmint

Retrieves project usage data from Crossmint.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1-alpha1/projects/:projectId/usage`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Get Usage](https://docs.crossmint.com/api-reference/admin/get-usage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `string` | yes | Enter the month in YYYY-MM format, for example `2026-04`. |
| `endDate` | query | `string` | no | Optional end month in YYYY-MM format, for example `2026-04`. |
