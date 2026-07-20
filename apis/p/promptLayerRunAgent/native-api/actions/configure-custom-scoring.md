# Configure Custom Scoring with PromptLayer Run Agent

Updates custom scoring for a PromptLayer evaluation.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/reports/:reportId/score-card`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Configure Custom Scoring](https://docs.promptlayer.com/reference/update-report-score-card)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reportId` | path | `number` | yes | ID of the evaluation pipeline report. |
| `column_names[]` | body | `array<string>` | yes | List of column names to include in score calculation. |
| `code` | body | `string` | no | Optional Python or JavaScript code for custom score calculation. |
| `code_language` | body | `string` | no | Language of the custom code: PYTHON or JAVASCRIPT. |
