# Generate Workflow Documents with ActiveMerge

Generates documents from a workflow in ActiveMerge.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/workflows/generate`
- **Base URL:** `https://app.activemerge.com`
- **Official documentation:** [Generate Workflow Documents](https://app.activemerge.com/api/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Object mapping workflow placeholders to values. |
| `format` | body | `string` | yes | Output format: pdf, docx, or pptx. Accepted values: `0`, `1`, `2`. |
| `workflow_id` | body | `string` | yes | Workflow ID to generate from. |
