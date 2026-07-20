# Generate Dynamic YAML Badge with Shields.io

Retrieves a badge image from YAML data in Shields.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/badge/dynamic/yaml`
- **Base URL:** `https://img.shields.io`
- **Official documentation:** [Generate Dynamic YAML Badge](https://shields.io/badges/dynamic-yaml-badge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL to a YAML document. |
| `query` | query | `string` | yes | JSONPath expression used to select the badge value. |
| `style` | query | `string` | no | Badge style. Supported values include flat, flat-square, plastic, for-the-badge, and social. |
