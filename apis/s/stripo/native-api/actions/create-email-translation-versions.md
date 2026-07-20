# Create Email Translation Versions with Stripo

Creates translation versions for an email in Stripo.

## Endpoint

- **Method:** `POST`
- **Path:** `/emails/:id/translation-versions`
- **Base URL:** `https://my.stripo.email/emailgeneration/v1`
- **Official documentation:** [Create Email Translation Versions](https://api.stripo.email/reference/createemailtranslationversions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The email ID. |
| `languages[]` | body | `array<string>` | yes | Language codes for translation versions. Send multiple values as a array. |
