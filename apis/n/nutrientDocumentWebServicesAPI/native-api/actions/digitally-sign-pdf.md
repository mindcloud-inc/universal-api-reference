# Digitally Sign PDF with Nutrient Document Web Services

Updates a PDF document with a digital signature in Nutrient Document Web Services API.

## Endpoint

- **Method:** `POST`
- **Path:** `/sign`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Digitally Sign PDF](https://www.nutrient.io/api/reference/public/#tag/Digital-Signatures/operation/sign-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | PDF file to sign. |
| `data` | body | `object` | no | Digital signature configuration. |
| `image` | body | `file` | no | Signature image file. |
| `graphicImage` | body | `file` | no | Graphic image file for signature appearance. |
