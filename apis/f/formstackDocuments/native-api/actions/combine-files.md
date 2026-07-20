# Combine Files with Formstack Documents

Combines files into one file in Formstack Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/combine`
- **Base URL:** `https://www.webmerge.me/api`
- **Official documentation:** [Combine Files](https://www.webmerge.me/developers/tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files[][contents]` | body | `string` | no | Base64-encoded contents for each file being combined |
| `files[][name]` | body | `string` | yes | Name for each file being combined |
| `files[][url]` | body | `string` | no | Remote URL for each file being combined |
| `output` | body | `string` | yes | Type of file to produce |
