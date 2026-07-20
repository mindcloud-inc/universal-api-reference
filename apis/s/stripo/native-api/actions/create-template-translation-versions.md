# Create Template Translation Versions with Stripo

Creates translation versions for a template in Stripo.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/:id/translation-versions`
- **Base URL:** `https://my.stripo.email/emailgeneration/v1`
- **Official documentation:** [Create Template Translation Versions](https://api.stripo.email/reference/createtemplatetranslationversions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The template ID. |
| `languages[]` | body | `array<string>` | yes | Language codes for translation versions. Send multiple values as a array. |
