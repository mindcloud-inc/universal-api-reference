# Parse Address String with Cloudmersive

Parses an address string in Cloudmersive.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/address/parse`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Parse Address String](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-parse-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AddressString` | body | `string` | no | Unstructured address string to parse. |
| `CapitalizationMode` | body | `string` | no | Optional capitalization mode for the parsed address. |
