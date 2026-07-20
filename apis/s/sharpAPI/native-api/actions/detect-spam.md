# Detect Spam with SharpAPI

Creates a spam detection job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/content/detect_spam`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Detect Spam](https://sharpapi.com/en/catalog/ai/content-marketing-automation/spam-detector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Provide the content to check whether it is spam. |
