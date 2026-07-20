# List Hypotheses with Convert

Retrieves hypotheses from a Convert project.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:account_id/projects/:project_id/hypotheses`
- **Base URL:** `https://api.convert.com/api/v2`
- **Official documentation:** [List Hypotheses](https://api.convert.com/doc/v2/#tag/Hypotheses/operation/getHypothesesList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Convert project ID. |
