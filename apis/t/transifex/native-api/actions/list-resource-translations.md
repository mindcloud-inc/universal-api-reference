# List Resource Translations with Transifex

## Endpoint

- **Method:** `GET`
- **Path:** `/resource_translations`
- **Base URL:** `https://rest.api.transifex.com`
- **Official documentation:** [List Resource Translations](https://developers.transifex.com/reference/get_resource-translations.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[language]` | query | `string` | yes | Return translations for this language id. |
| `filter[resource]` | query | `string` | yes | Return translations for this resource id. |
