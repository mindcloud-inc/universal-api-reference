# Complete Automation Run with Testmo

Marks an automation run as completed in Testmo.

## Endpoint

- **Method:** `POST`
- **Path:** `/automation/runs/{automation_run_id}/complete`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Complete Automation Run](https://support.testmo.com/hc/en-us/articles/37971158770957-Automation-Runs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `automation_run_id` | path | `number` | yes | ID of the automation run to complete. |
| `measure_elapsed` | body | `boolean` | no | Whether Testmo should compute elapsed time from run creation to completion. |
