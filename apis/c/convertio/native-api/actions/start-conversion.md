# Start Conversion with Convertio

Starts a conversion in Convertio.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert`
- **Base URL:** `https://api.convertio.co`
- **Official documentation:** [Start Conversion](https://developers.convertio.co/api/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | no | URL of the input file when input=url, or file content when input=raw/base64. Omit for input=upload. |
| `filename` | body | `string` | no | Input filename including extension. Required when input=raw/base64. |
| `input` | body | `string` | no | How the input file is provided. |
| `outputformat` | body | `string` | yes | Target file format for the conversion result. |
