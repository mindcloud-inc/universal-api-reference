# Docparser: Native API Reference

A consolidated summary of Docparser's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://docparser.com/api/
- **API base URL:** `https://api.docparser.com`

## Authentication

### API Key

Use your Docparser API key as a regular API key credential.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docparser.com/api/)

## API conventions

Responses from this API use JSON.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Fetch Document From URL](actions/fetch-document-from-url.md) | `POST /v2/document/fetch/:PARSER_ID` | [docs](https://docparser.com/api/#fetch-document-from-url) |
| [Fetch Document From URL With Remote ID](actions/fetch-document-from-url-with-remote-id.md) | `POST /v2/document/fetch/:PARSER_ID` | [docs](https://docparser.com/api/#fetch-document-from-url) |
| [Get Data Of Multiple Documents](actions/get-data-of-multiple-documents.md) | `GET /v1/results/:PARSER_ID` | [docs](https://docparser.com/api/#get-data-of-multiple-documents) |
| [Get Data Of Multiple Documents By Remote ID](actions/get-data-of-multiple-documents-by-remote-id.md) | `GET /v1/results/:PARSER_ID` | [docs](https://docparser.com/api/#get-data-of-multiple-documents) |
| [Get Data Of One Document](actions/get-data-of-one-document.md) | `GET /v1/results/:PARSER_ID/:DOCUMENT_ID` | [docs](https://docparser.com/api/#get-data-of-one-document) |
| [Get Data Of One Document Including Children](actions/get-data-of-one-document-including-children.md) | `GET /v1/results/:PARSER_ID/:DOCUMENT_ID` | [docs](https://docparser.com/api/#get-data-of-one-document) |
| [Get Document Status](actions/get-document-status.md) | `GET /v2/document/status/:PARSER_ID/:DOCUMENT_ID` | [docs](https://docparser.com/api/#document-status) |
| [Get Flat Data Of Multiple Documents](actions/get-flat-data-of-multiple-documents.md) | `GET /v1/results/:PARSER_ID` | [docs](https://docparser.com/api/#get-data-of-multiple-documents) |
| [Get Flat Data Of One Document](actions/get-flat-data-of-one-document.md) | `GET /v1/results/:PARSER_ID/:DOCUMENT_ID` | [docs](https://docparser.com/api/#get-data-of-one-document) |
| [Get Sorted Data Of Multiple Documents](actions/get-sorted-data-of-multiple-documents.md) | `GET /v1/results/:PARSER_ID` | [docs](https://docparser.com/api/#get-data-of-multiple-documents) |
| [List Document Parsers](actions/list-document-parsers.md) | `GET /v1/parsers` | [docs](https://docparser.com/api/#list-document-parsers) |
| [List Parser Model Layouts](actions/list-parser-model-layouts.md) | `GET /v1/parser/models/:PARSER_ID` | [docs](https://docparser.com/api/#list-parser-model-layouts) |
| [Ping](actions/ping.md) | `GET /v1/ping` | [docs](https://docparser.com/api/#authentication) |
| [Re-Integrate Data](actions/re-integrate-data.md) | `POST /v1/document/reintegrate/:PARSER_ID` | [docs](https://docparser.com/api/#re-integrate-data) |
| [Re-Parse Data](actions/re-parse-data.md) | `POST /v1/document/reparse/:PARSER_ID` | [docs](https://docparser.com/api/#re-parse-data) |
| [Upload Document By Content](actions/upload-document-by-content.md) | `POST /v1/document/upload/:PARSER_ID` | [docs](https://docparser.com/api/#upload-document-by-content) |
| [Upload Document By Content With Remote ID](actions/upload-document-by-content-with-remote-id.md) | `POST /v1/document/upload/:PARSER_ID` | [docs](https://docparser.com/api/#upload-document-by-content) |
| [Upload Document From Local Path](actions/upload-document-from-local-path.md) | `POST /v1/document/upload/:PARSER_ID` | [docs](https://docparser.com/api/#upload-document-from-local-path) |
| [Upload Document From Local Path With Remote ID](actions/upload-document-from-local-path-with-remote-id.md) | `POST /v1/document/upload/:PARSER_ID` | [docs](https://docparser.com/api/#upload-document-from-local-path) |
