# Update Transcript Evaluation with Voiceflow

Updates an existing transcript evaluation in Voiceflow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://analytics-api.voiceflow.com/v1/transcript-evaluation/:evaluationId`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Update Transcript Evaluation](https://docs.voiceflow.com/api-reference/transcript-evaluation/update-transcript-evaluation)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `evaluationId` | path | `string` | yes | ID of the transcript evaluation to target. |
| `name` | body | `string` | no | Name of the evaluation. |
| `description` | body | `string` | no | Description of the evaluation. |
| `enabled` | body | `boolean` | no | Whether the evaluation runs on every new transcript. |
| `prompt` | body | `string` | no | Prompt describing how the evaluation should be applied. |
| `truePrompt` | body | `string` | no | Prompt describing which transcripts should evaluate as true. |
| `falsePrompt` | body | `string` | no | Prompt describing which transcripts should evaluate as false. |
