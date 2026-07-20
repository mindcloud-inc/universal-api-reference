# List Sandbox Metrics with E2B

Retrieves metrics for sandboxes from E2B.

## Endpoint

- **Method:** `GET`
- **Path:** `/sandboxes/metrics`
- **Base URL:** `https://api.e2b.app`
- **Official documentation:** [List Sandbox Metrics](https://e2b.dev/docs/api-reference/sandboxes/list-sandbox-metrics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sandbox_ids` | query | `string<string>` | yes | Comma-separated list of sandbox IDs to get metrics for. Send multiple values as a string separated by `,`. |
