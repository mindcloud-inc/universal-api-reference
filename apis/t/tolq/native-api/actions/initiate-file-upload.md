# Initiate File Upload with Tolq

Initiates a file upload in Tolq.

## Endpoint

- **Method:** `POST`
- **Path:** `/translations/requests/upload`
- **Base URL:** `https://api.tolq.com/v1`
- **Official documentation:** [Initiate File Upload](https://docs.tolq.com/reference/initiate-a-file-upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_name` | body | `string` | yes | File name including supported extension such as csv, html, json, or xml. |
| `source_language_code` | body | `string` | yes | Two-letter ISO 639-1 source language code. |
| `separator` | body | `string` | no | Optional separator character for csv files. |
