# Detect Phone Numbers with SharpAPI

Creates a phone number detection job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/content/detect_phones`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Detect Phone Numbers](https://sharpapi.com/en/catalog/ai/content-marketing-automation/phone-numbers-detector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Provide the content from where the mobile number needs to be detected. |
