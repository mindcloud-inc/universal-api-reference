# Analyze email subject or body content and provide a performance report with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/ai-assistant/analyze`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Analyze email subject or body content and provide a performance report](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Type of content to analyze (subject or body) |
| `content` | body | `string` | yes | The email subject or body to analyze |
| `sender` | body | `string` | no | The sender persona |
| `audience` | body | `string` | yes | The target audience |
| `goal` | body | `string` | no | The goal of the email |
| `tone` | body | `string` | no | The tone of the email |
