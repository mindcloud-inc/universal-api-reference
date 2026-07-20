# Status By Spec Over Time with Cypress

Retrieves spec status rates over time from Cypress Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://cloud.cypress.io/enterprise-reporting/report`
- **Official documentation:** [Status By Spec Over Time](https://docs.cypress.io/cloud/integrations/data-extract-api#Status-by-spec-over-time)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `report_id` | query | `string` | no | Fixed Cypress report identifier for Status by spec over time. |
