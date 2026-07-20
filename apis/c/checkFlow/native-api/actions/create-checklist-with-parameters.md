# Create Checklist With Parameters with CheckFlow

## Endpoint

- **Method:** `POST`
- **Path:** `/api/checklist/create-with-parameters`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Create Checklist With Parameters](https://docs.checkflow.io/docs/api/checklists#create-checklist-with-parameters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateKey` | body | `string` | yes | The key of the template to create the checklist from. |
| `checklistName` | body | `string` | yes | The name for the new checklist. |
| `parameters[]` | body | `array<object>` | no | A list of parameter name and value pairs to set on creation. |
| `parameters[].parameterName` | body | `string` | yes | The name of the template parameter. |
| `parameters[].parameterValue` | body | `string` | yes | The value to assign to the template parameter. |
