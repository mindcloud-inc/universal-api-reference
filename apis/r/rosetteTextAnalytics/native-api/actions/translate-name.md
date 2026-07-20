# Translate Name with Rosette Text Analytics

## Endpoint

- **Method:** `POST`
- **Path:** `/name-translation`
- **Base URL:** `https://api.rosette.com/rest/v1`
- **Official documentation:** [Translate Name](https://docs.babelstreet.com/en/index-en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name to transliterate. |
| `targetLanguage` | body | `string` | yes | Three-letter ISO 639-3 target language code. |
| `sourceScript` | body | `string` | no | Script of the input name as a four-letter ISO 15924 code. |
| `sourceLanguageOfUse` | body | `string` | no | Language of the name as used in the input, as a three-letter ISO 639-3 code. |
| `sourceLanguageOfOrigin` | body | `string` | no | Native language the name originates in, as a three-letter ISO 639-3 code. |
| `targetScript` | body | `string` | no | Four-letter ISO 15924 target script code. |
| `entityType` | body | `string` | no | PERSON (default), LOCATION, or ORGANIZATION. |
| `targetScheme` | body | `string` | no | Advanced transliteration scheme abbreviation. |
