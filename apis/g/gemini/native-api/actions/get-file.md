# Get File with Gemini

Retrieves the metadata for a file from Gemini.

## Endpoint

- **Method:** `GET`
- **Path:** `v1beta/files/:fileId`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Get File](https://ai.google.dev/api/files#method:-files.get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `string` | yes | File ID segment (without `files/` prefix). |
