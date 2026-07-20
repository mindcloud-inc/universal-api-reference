# Tokenize Text with Rosette Text Analytics

## Endpoint

- **Method:** `POST`
- **Path:** `/tokens`
- **Base URL:** `https://api.rosette.com/rest/v1`
- **Official documentation:** [Tokenize Text](https://docs.babelstreet.com/en/index-en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | Text to process. |
| `contentUri` | body | `string` | no | URI to accessible content. Mutually exclusive with content. |
| `language` | body | `string` | no | Three-letter ISO 639-3 language code. |
