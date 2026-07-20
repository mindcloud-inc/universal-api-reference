# Create Automation Run with Testmo

Creates a new automation run in Testmo.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{project_id}/automation/runs`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Create Automation Run](https://support.testmo.com/hc/en-us/articles/37971158770957-Automation-Runs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | ID of the target project. |
| `name` | body | `string` | yes | Name of the new automation run. |
| `source` | body | `string` | yes | Name of the automation source for the new run. |
