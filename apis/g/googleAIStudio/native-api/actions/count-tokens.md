# Count Tokens with Google AI Studio

Counts prompt tokens for a Gemini model in Google AI Studio.

## Endpoint

- **Method:** `POST`
- **Path:** `v1beta/models/:model`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Count Tokens](https://ai.google.dev/api/tokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | path | `string` | yes | Required. Model endpoint token including suffix, for example `gemini-2.5-flash:countTokens`. |
| `contents[]` | body | `array<object>` | no | Optional prompt contents to tokenize. |
| `generateContentRequest` | body | `object` | no | Optional full GenerateContentRequest payload. |
