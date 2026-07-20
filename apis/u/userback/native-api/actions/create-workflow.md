# Create Workflow with Userback

Creates a new workflow in Userback.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflow`
- **Base URL:** `https://rest.userback.io/1.0`
- **Official documentation:** [Create Workflow](https://docs.userback.io/reference/createworkflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | body | `number` | yes | The project ID that will own the workflow. |
| `name` | body | `string` | yes | The workflow name. |
| `color` | body | `string` | yes | The workflow color in hex format. |
