# List Organization Workflow Statuses with Zeplin

Retrieves a list of organization workflow statuses from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{organization_id}/workflow_statuses`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Organization Workflow Statuses](https://docs.zeplin.dev/reference/getorganizationworkflowstatuses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | path | `string` | yes | Organization id |
