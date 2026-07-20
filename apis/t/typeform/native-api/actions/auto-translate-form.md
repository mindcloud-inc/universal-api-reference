# Auto-Translate Form with Typeform

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:formId/translations/:language/auto`
- **Base URL:** `https://api.typeform.com`
- **Official documentation:** [Auto-Translate Form](https://www.typeform.com/developers/create/reference/auto-translate-form/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Typeform form identifier. |
| `language` | path | `string` | yes | Language code. |
