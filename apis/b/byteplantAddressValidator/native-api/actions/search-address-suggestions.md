# Search Address Suggestions with Byteplant Address Validator

Finds address suggestions in Byteplant Address Validator.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/search`
- **Base URL:** `https://api.address-validator.net`
- **Official documentation:** [Search Address Suggestions](https://www.byteplant.com/address-validator/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Query` | query | `string` | yes | Freeform address text to match against Byteplant suggestions. |
| `CountryCode` | query | `string` | yes | Two-letter ISO 3166-1 country code. Use XX for international. |
| `MatchLevel` | query | `string` | no | Optional suggestion granularity: locality, street, building, or subbuilding. |
| `Locale` | query | `string` | no | Output language for countries with multiple postal languages. |
| `MaxResults` | query | `number` | no | Maximum number of suggestions to return. |
| `Timeout` | query | `number` | no | Request timeout in seconds. |
