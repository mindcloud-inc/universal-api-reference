# Create Transcript Evaluation with Voiceflow

Creates a new transcript evaluation in Voiceflow.

## Endpoint

- **Method:** `POST`
- **Path:** `https://analytics-api.voiceflow.com/v1/transcript-evaluation`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Create Transcript Evaluation](https://docs.voiceflow.com/api-reference/transcript-evaluation/create-transcript-evaluation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the evaluation. |
| `enabled` | body | `boolean` | yes | Whether this evaluation runs on new transcripts. |
| `prompt` | body | `string` | yes | Prompt describing how the LLM should apply this evaluation. |
| `type` | body | `string` | yes | Type of evaluation. |
| `truePrompt` | body | `string` | yes | Prompt describing which transcripts should evaluate as true. |
| `falsePrompt` | body | `string` | yes | Prompt describing which transcripts should evaluate as false. |
| `description` | body | `string` | no | Optional description of the evaluation. |
| `settings` | body | `object` | no | Optional model settings used when invoking this evaluation. |
