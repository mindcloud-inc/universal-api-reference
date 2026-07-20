# Compare Address Similarity with Rosette Text Analytics

## Endpoint

- **Method:** `POST`
- **Path:** `/address-similarity`
- **Base URL:** `https://api.rosette.com/rest/v1`
- **Official documentation:** [Compare Address Similarity](https://docs.babelstreet.com/en/index-en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address1` | body | `string` | yes | First address to compare. |
| `language` | body | `string` | no | Three-letter ISO 639-3 language code when known. |
| `address2` | body | `string` | yes | Second address to compare. |
