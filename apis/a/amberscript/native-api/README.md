# Amberscript: Native API Reference

A consolidated summary of Amberscript's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://amberscript.github.io/api-docs/
- **API base URL:** `https://api.amberscript.com/api`

## Authentication

### API Key

Connect Amberscript with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://amberscript.github.io/api-docs/)

## Pagination

Use `pageSize` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 0.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `sortDirection`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Glossary](actions/create-glossary.md) | `POST /glossary` | [docs](https://amberscript.github.io/api-docs/#create-a-glossary) |
| [Delete Glossary](actions/delete-glossary.md) | `DELETE /glossary/:glossaryId` | [docs](https://amberscript.github.io/api-docs/#delete-a-glossary) |
| [Delete Job](actions/delete-job.md) | `DELETE /jobs` | [docs](https://amberscript.github.io/api-docs/#delete-a-job) |
| [Export JSON](actions/export-json.md) | `GET /jobs/export-json` | [docs](https://amberscript.github.io/api-docs/#export-to-json) |
| [Export SRT](actions/export-srt.md) | `GET /jobs/export-srt` | [docs](https://amberscript.github.io/api-docs/#export-to-srt) |
| [Export STL](actions/export-stl.md) | `GET /jobs/export-stl` | [docs](https://amberscript.github.io/api-docs/#export-to-stl) |
| [Export TXT](actions/export-txt.md) | `GET /jobs/export-txt` | [docs](https://amberscript.github.io/api-docs/#export-to-text) |
| [Export VTT](actions/export-vtt.md) | `GET /jobs/export-vtt` | [docs](https://amberscript.github.io/api-docs/#export-to-vtt) |
| [Get Job Status](actions/get-job-status.md) | `GET /jobs/status` | [docs](https://amberscript.github.io/api-docs/#getting-the-status-of-a-transcription) |
| [List Glossaries](actions/list-glossaries.md) | `GET /glossary` | [docs](https://amberscript.github.io/api-docs/#get-a-list-of-glossaries) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs` | [docs](https://amberscript.github.io/api-docs/#get-list-of-jobs) |
| [Request Translated Subtitles](actions/request-translated-subtitles.md) | `POST /jobs/translatedSubtitles` | [docs](https://amberscript.github.io/api-docs/#request-translated-subtitles-for-an-existing-manual-39-perfect-39-captions-job) |
| [Update Glossary](actions/update-glossary.md) | `PUT /glossary/:glossaryId` | [docs](https://amberscript.github.io/api-docs/#update-a-glossary) |
| [Upload File](actions/upload-file.md) | `POST /jobs/upload-media` | [docs](https://amberscript.github.io/api-docs/#uploading-a-file) |
| [Upload File by URL](actions/upload-file-by-url.md) | `POST /jobs/upload-media-from-url` | [docs](https://amberscript.github.io/api-docs/#uploading-a-file-by-url) |
