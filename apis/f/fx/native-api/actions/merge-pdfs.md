# Merge PDFs with 1001fx

Merges up to three PDFs into one PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/mergepdfs`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Merge PDFs](https://1001fx.com/functions/mergepdfs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file1` | body | `file` | yes |
| `file2` | body | `file` | yes |
| `file3` | body | `file` | no |
