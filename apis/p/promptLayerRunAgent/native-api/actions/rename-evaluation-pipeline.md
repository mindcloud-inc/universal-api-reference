# Rename Evaluation Pipeline with PromptLayer Run Agent

Renames a PromptLayer evaluation pipeline.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/reports/:reportId/rename`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Rename Evaluation Pipeline](https://docs.promptlayer.com/reference/rename-report)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reportId` | path | `number` | yes | ID of the evaluation pipeline report to rename. |
| `name` | body | `string` | yes | New name for the evaluation pipeline. |
