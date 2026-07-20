# Enhance Speech Prompt with deAPI

Enhances a text-to-speech prompt in deAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/client/prompt/speech`
- **Base URL:** `https://api.deapi.ai`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lang_code` | body | `string` | no | Optional language code for speech enhancement. |
| `prompt` | body | `string` | no | Speech prompt to enhance. |
