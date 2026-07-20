# Validate VAT Number with 44API

Validates a VAT number with 44API and returns company details.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook/validate-vat`
- **Base URL:** `https://api.44api.dev`
- **Official documentation:** [Validate VAT Number](https://docs.44api.dev)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vatNumber` | body | `string` | yes | VAT number with or without country prefix. |
| `countryCode` | body | `string` | yes | ISO 2-letter country code. |
