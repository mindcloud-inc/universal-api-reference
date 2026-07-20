# Validate String Format with 1001fx

Validates a string against a supported format.

## Endpoint

- **Method:** `POST`
- **Path:** `/data/validatestringformat`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Validate String Format](https://1001fx.com/functions/validatestringformat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | body | `string` | yes | String format to validate against. |
| `input` | body | `string` | yes | Input value to validate. |
| `options` | body | `object` | no | — |
