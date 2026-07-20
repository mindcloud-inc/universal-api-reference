# List Projects with DoneDone

Retrieves projects from DoneDone.

## Endpoint

- **Method:** `GET`
- **Path:** `/:account_id/internal-projects/for-selection`
- **Base URL:** `https://2.donedone.com/public-api`
- **Official documentation:** [List Projects](https://donedone.com/help-docs/public-api-webhooks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | DoneDone account ID. |
