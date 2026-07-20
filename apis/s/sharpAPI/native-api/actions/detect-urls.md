# Detect Urls with SharpAPI

Creates a URL detection job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/content/detect_urls`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Detect Urls](https://sharpapi.com/en/catalog/ai/content-marketing-automation/urls-detector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Provide the content from where URLs need to be detected. |
