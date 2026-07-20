# Generate Endpoint Badge with Shields.io

Retrieves a badge image from a JSON endpoint in Shields.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/endpoint`
- **Base URL:** `https://img.shields.io`
- **Official documentation:** [Generate Endpoint Badge](https://shields.io/badges/endpoint-badge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL to a JSON endpoint returning the Shields endpoint badge schema. |
| `style` | query | `string` | no | Badge style. Supported values include flat, flat-square, plastic, for-the-badge, and social. |
