# Find Semantically Similar Terms with Rosette Text Analytics

## Endpoint

- **Method:** `POST`
- **Path:** `/semantics/similar`
- **Base URL:** `https://api.rosette.com/rest/v1`
- **Official documentation:** [Find Semantically Similar Terms](https://docs.babelstreet.com/en/index-en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Input term or text to compare in semantic space. |
| `language` | body | `string` | no | Three-letter ISO 639-3 language code for the input. |
| `options.resultLanguages[]` | body | `array<string>` | yes | One or more three-letter language codes to return similar terms in. |
| `options.count` | body | `number` | no | Number of similar terms to return per result language, from 1 to 50. |
