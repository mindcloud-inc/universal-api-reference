# Iteratively improve an existing AI-generated email template with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/ai-template/refine/{emailId}`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Iteratively improve an existing AI-generated email template](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailId` | path | `string` | yes | The ID of the AI-generated email to refine |
| `refinementPrompt` | body | `string` | yes | Instructions for refining the existing template |
