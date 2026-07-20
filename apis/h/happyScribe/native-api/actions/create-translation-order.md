# Create Translation Order with HappyScribe

Creates a translation order in HappyScribe.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/translation`
- **Base URL:** `https://www.happyscribe.com/api/v1`
- **Official documentation:** [Create Translation Order](https://dev.happyscribe.com/sections/product/#orders-create-a-translation-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `confirm` | body | `boolean` | no | When true, submit the translation order immediately if there are no errors. |
| `service` | body | `string` | no | Service type: auto or pro. |
| `source_transcription_id` | body | `string` | yes | Source transcription to translate. |
| `target_languages[]` | body | `array<string>` | yes | One or more target language codes. |
