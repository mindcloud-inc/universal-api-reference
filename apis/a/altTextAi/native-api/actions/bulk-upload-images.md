# Bulk Upload Images with AltText.Ai

Bulk uploads image URLs for alt text generation in AltText.Ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/images/bulk_create`
- **Base URL:** `https://alttext.ai/api/v1`
- **Official documentation:** [Bulk Upload Images](https://alttext.ai/apidocs#tag/Images/operation/bulk-create)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Optional email address to receive bulk upload results. |
| `file` | body | `file` | yes | CSV file containing image URLs to upload for bulk processing. |
