# Generate Dynamic Regex Badge with Shields.io

Retrieves a badge image from regex-matched text in Shields.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/badge/dynamic/regex`
- **Base URL:** `https://img.shields.io`
- **Official documentation:** [Generate Dynamic Regex Badge](https://shields.io/badges/dynamic-regex-badge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL to a text file to search. |
| `search` | query | `string` | yes | RE2 expression used to extract badge text from the document. |
| `replace` | query | `string` | no | Optional replacement string for the regex match. |
| `style` | query | `string` | no | Badge style. Supported values include flat, flat-square, plastic, for-the-badge, and social. |
