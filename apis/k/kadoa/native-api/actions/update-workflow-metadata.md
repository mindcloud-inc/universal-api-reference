# Update Workflow Metadata with Kadoa

## Endpoint

- **Method:** `PUT`
- **Path:** `/v4/workflows/:workflowId/metadata`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Update Workflow Metadata](https://docs.kadoa.com/api-reference/workflows/update-workflow-metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowId` | path | `string` | yes | Workflow ID |
| `name` | body | `string` | no | Workflow name |
| `description` | body | `string` | no | Description |
| `tags` | body | `string` | no | JSON array of tags |
| `updateInterval` | body | `string` | no | Interval: ONLY_ONCE, HOURLY, DAILY, WEEKLY, MONTHLY, CUSTOM |
| `maxPages` | body | `number` | no | Max pages |
| `maxDepth` | body | `number` | no | Max depth |
| `navigationMode` | body | `string` | no | Navigation mode |
