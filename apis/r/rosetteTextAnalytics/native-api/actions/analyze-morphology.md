# Analyze Morphology with Rosette Text Analytics

## Endpoint

- **Method:** `POST`
- **Path:** `/morphology/:morphoFeature`
- **Base URL:** `https://api.rosette.com/rest/v1`
- **Official documentation:** [Analyze Morphology](https://docs.babelstreet.com/en/index-en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | Text to process. |
| `contentUri` | body | `string` | no | URI to accessible content. Mutually exclusive with content. |
| `language` | body | `string` | no | Three-letter ISO 639-3 language code. |
| `morphoFeature` | path | `string` | yes | Morphology feature path segment. Use complete for all supported morphology features. |
