# Create Workflow with Shuffler

Creates a new workflow in Shuffler.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflows`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Create Workflow](https://shuffler.io/docs/API#create-new-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | yes | Workflow description. |
| `name` | body | `string` | yes | Workflow name. |
