# Analyze File With AI with PDF-app

Retrieves AI analysis from a file in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/ai`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Analyze File With AI](https://pdf-app.net/apidocumentation?type=ai)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input_text` | body | `string` | no | Instruction or question for the AI analyzer. |
| `fileUrl[]` | body | `array<string>` | no | Optional file URLs to analyze alongside the prompt. |
| `examples` | body | `string` | no | Optional extra examples or guidance for the AI model. |
| `async` | body | `boolean` | no | Whether to run the AI analysis asynchronously. |
| `type` | body | `string` | no | Model selector such as model1, model2, or model3. |
| `temperature` | body | `number` | no | Controls response variability between 0 and 1. |
