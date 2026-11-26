# List Flow Run Execution Logs with Celigo

## Endpoint

- **Method:** `GET`
- **Path:** `/flows/:flowId/jobs/:jobId/logs`
- **Base URL:** `https://{apiHost}/v1`
- **Official documentation:** [List Flow Run Execution Logs](https://developer.celigo.com/api/api-reference/integrations-and-flows/flows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `flowId` | path | `list<string>` | yes | Flow that ran. |
| `jobId` | path | `string` | yes | Flow-run job ID (a job of type Flow). |
| `status` | query | `list<string>` | no | Only return entries with this record outcome. Accepted values: `error`, `ignore`, `success`. |
| `_expOrImpId[]` | query | `array<string>` | no | Only return entries produced by these export or import steps. Send multiple values as a string separated by `,`. |
| `traceKeyPrefix` | query | `string` | no | Only return entries whose trace key starts with this value. |
| `sortOrder` | query | `list<string>` | no | Order by start time. Defaults to newest first. Accepted values: `asc`, `desc`. |
