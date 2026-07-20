# Run Tool with Superglue

Runs a tool in Superglue.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/:toolId/run`
- **Base URL:** `https://api.superglue.ai/v1`
- **Official documentation:** [Run Tool](https://docs.superglue.cloud/api-reference/tools/run-a-tool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `toolId` | path | `string` | yes | ID of the Superglue tool to run. |
| `runId` | body | `string` | no | Optional pre-generated run ID for idempotency and tracking. |
| `inputs` | body | `object` | no | Tool-specific input parameters. |
| `options` | body | `object` | no | Execution options for the run. |
| `options.async` | body | `boolean` | no | Return immediately and execute asynchronously when true. |
| `options.timeout` | body | `number` | no | Request timeout in milliseconds. |
| `options.webhookUrl` | body | `string` | no | Callback URL or tool:{toolId} chain target when the run finishes. |
| `options.mode` | body | `list` | no | Execution mode for system resolution. Accepted values: `dev`, `prod`. |
| `options.requestSource` | body | `list` | no | Override the request source identifier. Accepted values: `cli`, `frontend`, `mcp`. |
| `options.traceId` | body | `string` | no | Custom trace ID for log tracking. |
