# 3Scribe: Native API Reference

A consolidated summary of 3Scribe's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://helpcentre.3scri.be/developers/api/
- **API base URL:** `https://api.3scri.be`

## Authentication

### API Key

Authenticate 3Scribe requests with the account API key sent in the APIKey header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
APIKey: <apiKey>
```

[Official authentication documentation](https://helpcentre.3scri.be/developers/api/)

## Pagination

Use `perpage` in the query string to set the page size (default 10; accepted range 10–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order` in the query string. Set the direction separately with `direction`. Use `1` for ascending order and `2` for descending order. Only one sort field is accepted.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Transcription Job Via Pre-Signed URL](actions/create-transcription-job-via-pre-signed-url.md) | `POST /transcribe` | [docs](https://helpcentre.3scri.be/developers/api/) |
| [Create Transcription Job Via Public URL](actions/create-transcription-job-via-public-url.md) | `POST /transcribe` | [docs](https://helpcentre.3scri.be/developers/api/) |
| [Delete Transcription Job](actions/delete-transcription-job.md) | `DELETE /jobs/:jobid` | [docs](https://helpcentre.3scri.be/developers/api/) |
| [Get Transcription Job](actions/get-transcription-job.md) | `GET /jobs/:jobid` | [docs](https://helpcentre.3scri.be/developers/api/) |
| [List Transcription Jobs](actions/list-transcription-jobs.md) | `GET /jobs` | [docs](https://helpcentre.3scri.be/developers/api/) |
