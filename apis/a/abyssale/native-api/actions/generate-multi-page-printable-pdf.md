# Generate Multi-Page Printable PDF with Abyssale

Generates a multi-page printable PDF in Abyssale.

## Endpoint

- **Method:** `POST`
- **Path:** `/async/banner-builder/:design_id/generate`
- **Base URL:** `https://api.abyssale.com`
- **Official documentation:** [Generate Multi-Page Printable PDF](https://developers.abyssale.com/rest-api/generation/asynchronous-generation/generate-multi-page-pdf-for-printing)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `design_id` | path | `string` | yes |
| `pages` | body | `object` | yes |
| `print` | body | `object` | no |
