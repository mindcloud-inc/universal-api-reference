# Fix and optimize manual email content using AI and analysis report (paid users only) with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/ai-assistant/fix`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Fix and optimize manual email content using AI and analysis report (paid users only)](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Type of content to fix (subject or body) |
| `content` | body | `string` | yes | The email subject or body to fix |
| `analysis[]` | body | `array<object>` | yes | The analysis report array Send multiple values as a array. |
