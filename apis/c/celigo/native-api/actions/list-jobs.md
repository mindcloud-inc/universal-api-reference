# List Jobs with Celigo

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs`
- **Base URL:** `https://{apiHost}/v1`
- **Official documentation:** [List Jobs](https://developer.celigo.com/api/api-reference/monitoring/jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_integrationId` | query | `list<string>` | no | Only return jobs for this integration. Send it with Flow ID when the flow belongs to an integration. |
| `_flowId` | query | `list<string>` | no | Only return jobs for this flow. Pick from List Flows. |
| `status` | query | `list<string>` | no | Only return jobs in this status. Accepted values: `canceled`, `canceling`, `completed`, `failed`, `queued`, `retrying`, `running`. |
| `type` | query | `list<string>` | no | Job type. Flow, Retry and Bulk Retry are parent (run-level) jobs; Export, Import and Tool are step jobs and need Flow Job ID, Export ID or Import ID. Accepted values: `bulk_retry`, `export`, `flow`, `import`, `retry`, `tool`. |
| `createdAt_gte` | query | `date` | no | Only return jobs created at or after this time (ISO 8601). |
| `createdAt_lte` | query | `date` | no | Only return jobs created at or before this time. To page, pass the last job's createdAt minus 1 ms. |
| `_flowJobId` | query | `string` | no | Parent flow-run job ID. Required for Export, Import and Tool step jobs. |
| `_exportId` | query | `string` | no | Only return jobs for this export step. |
| `_importId` | query | `string` | no | Only return jobs for this import step. |
| `numError_gte` | query | `number` | no | Only return jobs with at least this many errors. |
| `numError_lte` | query | `number` | no | Only return jobs with at most this many errors. |
| `numSuccess_gte` | query | `number` | no | Only return jobs with at least this many successful records. |
| `numSuccess_lte` | query | `number` | no | Only return jobs with at most this many successful records. |
| `numIgnore_gte` | query | `number` | no | Only return jobs with at least this many ignored records. |
| `numIgnore_lte` | query | `number` | no | Only return jobs with at most this many ignored records. |
