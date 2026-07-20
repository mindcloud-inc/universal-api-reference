# Get Hypothesis with Convert

Retrieves a hypothesis from a Convert project.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/projects/:project_id/hypotheses/:hypothesis_id`
- **Base URL:** `https://api.convert.com/api/v2`
- **Official documentation:** [Get Hypothesis](https://api.convert.com/doc/v2/#tag/Hypotheses/operation/getHypothesis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Convert project ID. |
| `hypothesis_id` | path | `string` | yes | Convert hypothesis ID. |
