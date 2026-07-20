# List Workflow Statuses with DoneDone

Retrieves workflow statuses from DoneDone.

## Endpoint

- **Method:** `GET`
- **Path:** `/:account_id/workflows/:workflow_id/statuses`
- **Base URL:** `https://2.donedone.com/public-api`
- **Official documentation:** [List Workflow Statuses](https://donedone.com/help-docs/public-api-webhooks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | DoneDone account ID. |
| `workflow_id` | path | `number` | yes | DoneDone workflow ID. |
