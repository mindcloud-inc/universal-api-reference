# List Project Statuses with DoneDone

Retrieves project statuses from DoneDone.

## Endpoint

- **Method:** `GET`
- **Path:** `/:account_id/internal-projects/:internal_project_id/statuses`
- **Base URL:** `https://2.donedone.com/public-api`
- **Official documentation:** [List Project Statuses](https://donedone.com/help-docs/public-api-webhooks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | DoneDone account ID. |
| `internal_project_id` | path | `number` | yes | DoneDone internal project ID. |
