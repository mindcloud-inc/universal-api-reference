# Generate a new AI email template from a natural language prompt with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/ai-template/generate`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Generate a new AI email template from a natural language prompt](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Natural language description of the email template to generate |
| `audience` | body | `string` | no | The target audience for the email |
| `tone` | body | `string` | no | The desired tone of the email |
| `goal` | body | `string` | no | The goal of the email campaign |
