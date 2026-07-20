# Generate Dynamic JSON Badge with Shields.io

Retrieves a badge image from JSON data in Shields.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/badge/dynamic/json`
- **Base URL:** `https://img.shields.io`
- **Official documentation:** [Generate Dynamic JSON Badge](https://shields.io/badges/dynamic-json-badge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL to a JSON document. |
| `query` | query | `string` | yes | JSONPath expression used to select the badge value. |
| `style` | query | `string` | no | Badge style. Supported values include flat, flat-square, plastic, for-the-badge, and social. |
