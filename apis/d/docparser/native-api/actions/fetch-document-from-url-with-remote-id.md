# Fetch Document From URL With Remote ID with Docparser

Fetches a document from a URL into a Docparser parser and assigns a remote ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/document/fetch/:PARSER_ID`
- **Base URL:** `https://api.docparser.com`
- **Official documentation:** [Fetch Document From URL With Remote ID](https://docparser.com/api/#fetch-document-from-url)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `PARSER_ID` | path | `string` | yes |
| `url` | body | `string` | yes |
| `remote_id` | body | `string` | yes |
