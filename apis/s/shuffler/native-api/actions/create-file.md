# Create File with Shuffler

Creates a file in Shuffler.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/create`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Create File](https://shuffler.io/docs/API#create-a-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | File name. |
| `labels[]` | body | `array` | no | Optional labels array. |
| `namespace` | body | `string` | no | Optional namespace. |
| `org_id` | body | `string` | yes | Organization identifier. |
| `workflow_id` | body | `string` | yes | Workflow identifier. |
