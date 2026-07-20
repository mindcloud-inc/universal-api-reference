# Translate Post with Ayrshare

Translates a post in Ayrshare.

## Endpoint

- **Method:** `POST`
- **Path:** `/generate/translate`
- **Base URL:** `https://api.ayrshare.com/api`
- **Official documentation:** [Translate Post](https://www.ayrshare.com/docs/apis/generate/translate-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text to translate. |
| `lang` | body | `string` | yes | ISO language code to translate text into, such as es or fr. |
