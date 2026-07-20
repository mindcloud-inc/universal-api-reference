# Create Project Score with Braintrust

Creates a new project score in Braintrust.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/project_score`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Create Project Score](https://www.braintrust.dev/docs/api-reference/project-scores/create-project-score)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | Project id. |
| `name` | body | `string` | yes | Project score name. |
| `score_type` | body | `string` | yes | Project score type. |
