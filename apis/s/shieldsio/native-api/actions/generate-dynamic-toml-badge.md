# Generate Dynamic TOML Badge with Shields.io

Retrieves a badge image from TOML data in Shields.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/badge/dynamic/toml`
- **Base URL:** `https://img.shields.io`
- **Official documentation:** [Generate Dynamic TOML Badge](https://shields.io/badges/dynamic-toml-badge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL to a TOML document. |
| `query` | query | `string` | yes | JSONPath expression used to select the badge value. |
| `style` | query | `string` | no | Badge style. Supported values include flat, flat-square, plastic, for-the-badge, and social. |
