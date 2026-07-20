# Extract Product With Custom Attributes From HTTP with Automatic Data Extraction

Extracts product data and custom attributes from HTTP in Automatic Data Extraction.

## Endpoint

- **Method:** `POST`
- **Path:** `/extract`
- **Base URL:** `https://api.zyte.com/v1`
- **Official documentation:** [Extract Product With Custom Attributes From HTTP](https://docs.zyte.com/zyte-api/usage/extract/custom-attributes.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customAttributes` | body | `object` | yes | Custom attribute schema to extract. |
| `url` | body | `string` | yes | Absolute URL to extract data from. |
