# Batch Analyze Emails with Opportify

Creates an asynchronous email analysis job in Opportify.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/batch`
- **Base URL:** `https://api.opportify.ai/insights/v1`
- **Official documentation:** [Batch Analyze Emails](https://www.opportify.ai/docs/api/api-reference/batch-analyze-emails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Array of email addresses to analyze. |
| `name` | body | `string` | no | Optional name for the batch job. |
| `enableAI` | body | `boolean` | no | Enable AI-based analysis for insights. |
| `enableAutoCorrection` | body | `boolean` | no | Controls email auto-correction behavior for batch processing. Default: `false`.  - When set to `true`: The system will automatically apply corrections when highly confident. The analysis will be performed on corrected email addresses. - When set to `false`: The system will still suggest corrections in the results, but the analysis will remain based on the original email addresses provided. |
