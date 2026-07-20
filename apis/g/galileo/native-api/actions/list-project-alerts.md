# List Project Alerts with Galileo

Finds alerts for a Galileo project.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:project_id/alerts`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [List Project Alerts](https://docs.galileo.ai/api-reference/log-stream-alerts/list-alerts-by-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Galileo project UUID. |
