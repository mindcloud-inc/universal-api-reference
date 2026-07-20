# Extract Text From URL with PDF API Hub

## Endpoint

- **Method:** `POST`
- **Path:** `/extract-text-from-url`
- **Base URL:** `https://api.prefillpdf.com`
- **Official documentation:** [Extract Text From URL](https://api.prefillpdf.com/docs#/PDF%20Tools/extract_text_from_url_endpoint_extract_text_from_url_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_url` | query | `string` | yes | Public or signed PDF URL to download. |
| `inline` | query | `boolean` | no | Return text inline instead of a file. |
