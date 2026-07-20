# Perform a detailed analysis of email content and provide manual recommendations (paid users only) with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/ai-assistant/detailed-analysis`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Perform a detailed analysis of email content and provide manual recommendations (paid users only)](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Type of content to analyze (subject or body) |
| `content` | body | `string` | yes | The email subject or body to analyze |
| `sender` | body | `string` | no | The sender persona |
| `audience` | body | `string` | yes | The target audience |
| `goal` | body | `string` | no | The goal of the email |
| `tone` | body | `string` | no | The tone of the email |
