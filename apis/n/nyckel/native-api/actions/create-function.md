# Create Function with Nyckel

Creates a new function in Nyckel.

## Endpoint

- **Method:** `POST`
- **Path:** `/functions`
- **Base URL:** `https://www.nyckel.com/v1`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Human-readable function name. |
| `input` | body | `string` | yes | Input type for the function. |
| `output` | body | `string` | yes | Output type for the function. |
