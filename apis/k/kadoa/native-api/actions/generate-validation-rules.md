# Generate Validation Rules with Kadoa

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/data-validation/rules/actions/generate`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Generate Validation Rules](https://docs.kadoa.com/api-reference/data-validation/generate-rules)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `selectedColumns` | body | `string` | no | JSON array of columns |
| `userPrompt` | body | `string` | yes | Description of rules to generate |
| `workflowId` | body | `string` | yes | Workflow ID |
