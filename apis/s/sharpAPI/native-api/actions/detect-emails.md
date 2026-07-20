# Detect Emails with SharpAPI

Creates an email detection job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/content/detect_emails`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Detect Emails](https://sharpapi.com/en/catalog/ai/content-marketing-automation/emails-detector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Provide the content from where email addresses need to be detected. |
