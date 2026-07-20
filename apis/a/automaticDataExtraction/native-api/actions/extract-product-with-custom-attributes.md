# Extract Product With Custom Attributes with Automatic Data Extraction

Extracts product data and custom attributes in Automatic Data Extraction.

## Endpoint

- **Method:** `POST`
- **Path:** `/extract`
- **Base URL:** `https://api.zyte.com/v1`
- **Official documentation:** [Extract Product With Custom Attributes](https://docs.zyte.com/zyte-api/usage/extract/custom-attributes.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customAttributes` | body | `object` | yes | Custom attribute schema to extract alongside the product result. |
| `url` | body | `string` | yes | Absolute URL to extract data from. |
