# Generate Semantic Vector with Rosette Text Analytics

## Endpoint

- **Method:** `POST`
- **Path:** `/semantics/vector`
- **Base URL:** `https://api.rosette.com/rest/v1`
- **Official documentation:** [Generate Semantic Vector](https://docs.babelstreet.com/en/index-en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | Text to process. |
| `contentUri` | body | `string` | no | URI to accessible content. Mutually exclusive with content. |
| `language` | body | `string` | no | Three-letter ISO 639-3 language code. |
| `options.perToken` | body | `boolean` | no | If true, return a vector for each individual token. |
| `options.embeddingsMode` | body | `string` | no | Embeddings generation mode, such as GEN_1 or GEN_2. |
