# Simpleen Translation: Native API Reference

A consolidated summary of Simpleen Translation's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://simpleen.io/documentation/api-reference
- **API base URL:** `https://api.simpleen.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://simpleen.io/documentation/api-reference)

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create File](actions/create-file.md) | `POST /files` | [docs](https://simpleen.io/documentation/api-reference#file) |
| [Create Glossary](actions/create-glossary.md) | `POST /glossaries` | [docs](https://simpleen.io/documentation/api-reference#glossary) |
| [Create Segment](actions/create-segment.md) | `POST /segments` | [docs](https://simpleen.io/documentation/api-reference#post-segments) |
| [Delete File](actions/delete-file.md) | `DELETE /files/:id` | [docs](https://simpleen.io/documentation/api-reference#postputdelete-filesid) |
| [Delete Glossary](actions/delete-glossary.md) | `DELETE /glossaries/:id` | [docs](https://simpleen.io/documentation/api-reference#postputdelete-glossariesid) |
| [Delete Segment](actions/delete-segment.md) | `DELETE /segments/:id` | [docs](https://simpleen.io/documentation/api-reference#putdelete-segmentsid) |
| [Get File](actions/get-file.md) | `GET /files/:id` | [docs](https://simpleen.io/documentation/api-reference#get-filesid) |
| [Get Glossary](actions/get-glossary.md) | `GET /glossaries/:id` | [docs](https://simpleen.io/documentation/api-reference#get-glossariesid) |
| [Get Language](actions/get-language.md) | `GET /languages/:id` | [docs](https://simpleen.io/documentation/api-reference#language) |
| [Get Segment](actions/get-segment.md) | `GET /segments/:id` | [docs](https://simpleen.io/documentation/api-reference#get-segmentsid) |
| [List Files](actions/list-files.md) | `GET /files` | [docs](https://simpleen.io/documentation/api-reference#get-files) |
| [List Glossaries](actions/list-glossaries.md) | `GET /glossaries` | [docs](https://simpleen.io/documentation/api-reference#get-glossaries) |
| [List Languages](actions/list-languages.md) | `GET /languages` | [docs](https://simpleen.io/documentation/api-reference#get-languages) |
| [List Segments](actions/list-segments.md) | `GET /segments` | [docs](https://simpleen.io/documentation/api-reference#get-segments) |
| [Update File](actions/update-file.md) | `PUT /files/:id` | [docs](https://simpleen.io/documentation/api-reference#postputdelete-filesid) |
| [Update Glossary](actions/update-glossary.md) | `PUT /glossaries/:id` | [docs](https://simpleen.io/documentation/api-reference#postputdelete-glossariesid) |
| [Update Segment](actions/update-segment.md) | `PUT /segments/:id` | [docs](https://simpleen.io/documentation/api-reference#putdelete-segmentsid) |
