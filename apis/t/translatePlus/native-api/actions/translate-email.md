# Translate Email with TranslatePlus

Translates email subject and HTML body in TranslatePlus.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/translate/email`
- **Base URL:** `https://api.translateplus.io`
- **Official documentation:** [Translate Email](https://docs.translateplus.io/reference/v2/translation/translate-email)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `subject` | body | `string` | yes |
| `email_body` | body | `string` | yes |
| `source` | body | `string` | yes |
| `target` | body | `string` | yes |
