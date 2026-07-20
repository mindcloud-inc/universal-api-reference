# Fetch Project Logs with Braintrust

Retrieves events from project logs in Braintrust.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/project_logs/:project_id/fetch`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Fetch Project Logs](https://braintrust.dev/docs/api-reference/logs/fetch-project-logs-get-form.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id. |
