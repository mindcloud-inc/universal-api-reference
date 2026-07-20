# Generate Dynamic XML Badge with Shields.io

Retrieves a badge image from XML data in Shields.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/badge/dynamic/xml`
- **Base URL:** `https://img.shields.io`
- **Official documentation:** [Generate Dynamic XML Badge](https://shields.io/badges/dynamic-xml-badge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL to an XML document. |
| `query` | query | `string` | yes | XPath expression used to select the badge value. |
| `style` | query | `string` | no | Badge style. Supported values include flat, flat-square, plastic, for-the-badge, and social. |
