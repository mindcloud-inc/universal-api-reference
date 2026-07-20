# Create Project Tag with Braintrust

Creates a new project tag in Braintrust.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/project_tag`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Create Project Tag](https://www.braintrust.dev/docs/api-reference/project-tags/create-project-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | Project id. |
| `name` | body | `string` | yes | Project tag name. |
