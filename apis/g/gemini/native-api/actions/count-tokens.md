# Count Tokens with Gemini

Counts tokens for content in Gemini.

## Endpoint

- **Method:** `POST`
- **Path:** `v1beta/models/:model`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Count Tokens](https://ai.google.dev/api/tokens#method:-models.counttokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | path | `string` | yes | Required. Model endpoint token including suffix, for example gemini-2.5-flash:countTokens. |
| `contents[]` | body | `array<object>` | no | Optional prompt contents to tokenize. |
| `generateContentRequest` | body | `object` | no | Optional full GenerateContentRequest payload (mutually exclusive with contents). |
