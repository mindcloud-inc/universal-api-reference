# List Project Priorities with DoneDone

Retrieves project priorities from DoneDone.

## Endpoint

- **Method:** `GET`
- **Path:** `/:account_id/internal-projects/:internal_project_id/priorities`
- **Base URL:** `https://2.donedone.com/public-api`
- **Official documentation:** [List Project Priorities](https://donedone.com/help-docs/public-api-webhooks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | DoneDone account ID. |
| `internal_project_id` | path | `number` | yes | DoneDone internal project ID. |
