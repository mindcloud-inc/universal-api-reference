# Analyze Call With AI with Bland AI

Retrieves AI analysis for a call in Bland AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/calls/{call_id}/analyze`
- **Base URL:** `https://api.bland.ai`
- **Official documentation:** [Analyze Call With AI](https://docs.bland.ai/api-v1/post/calls-id-analyze)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `call_id` | path | `string` | yes |
| `goal` | body | `string` | yes |
| `questions` | body | `object<string>` | yes |
