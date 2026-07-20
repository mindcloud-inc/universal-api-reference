# List Workflows with DoneDone

Retrieves workflows from DoneDone.

## Endpoint

- **Method:** `GET`
- **Path:** `/:account_id/workflows/for-selection`
- **Base URL:** `https://2.donedone.com/public-api`
- **Official documentation:** [List Workflows](https://donedone.com/help-docs/public-api-webhooks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | DoneDone account ID. |
