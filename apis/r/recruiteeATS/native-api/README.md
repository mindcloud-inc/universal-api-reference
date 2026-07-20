# Recruitee ATS: Native API Reference

A consolidated summary of Recruitee ATS's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://docs.recruitee.com/reference/getting-started
- **API base URL:** `https://api.recruitee.com`

## Authentication

### API Key

Use a personal Recruitee API token to access the ATS API.

### Credentials

- **API Key:** `apiKey` · required
- **Company ID:** `companyId` · required · Numeric Recruitee company ID used in ATS API paths.
- **Company Subdomain:** `companySubdomain` · optional · Company careers subdomain without .recruitee.com.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.recruitee.com/en/articles/8213076-faq-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `offers`. The current page number is read from `meta.page`.

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Candidate](actions/create-candidate.md) | `POST /c/:company_id/candidates` | [docs](https://docs.recruitee.com/reference/candidates-post) |
| [Create Offer](actions/create-offer.md) | `POST /c/:company_id/offers` | [docs](https://docs.recruitee.com/reference/offersid-post) |
| [Delete Candidate](actions/delete-candidate.md) | `DELETE /c/:company_id/candidates/:id` | [docs](https://docs.recruitee.com/reference/candidatesid-delete) |
| [Delete Offer](actions/delete-offer.md) | `DELETE /c/:company_id/offers/:id` | [docs](https://docs.recruitee.com/reference/offersid-delete) |
| [Get Candidate](actions/get-candidate.md) | `GET /c/:company_id/candidates/:id` | [docs](https://docs.recruitee.com/reference/candidatesid-get) |
| [Get Offer](actions/get-offer.md) | `GET /c/:company_id/offers/:id` | [docs](https://docs.recruitee.com/reference/offersid-get) |
| [List Candidate Notes](actions/list-candidate-notes.md) | `GET /c/:company_id/candidates/:id/notes` | [docs](https://docs.recruitee.com/reference/candidatesidnotes) |
| [List Candidates](actions/list-candidates.md) | `GET /c/:company_id/candidates` | [docs](https://docs.recruitee.com/reference/candidates-get) |
| [List Departments](actions/list-departments.md) | `GET /c/:company_id/departments` | [docs](https://docs.recruitee.com/reference/departments-get) |
| [List Locations](actions/list-locations.md) | `GET /c/:company_id/locations` | [docs](https://docs.recruitee.com/reference/locations) |
| [List Offers](actions/list-offers.md) | `GET /c/:company_id/offers` | [docs](https://docs.recruitee.com/reference/offers-get) |
| [Search Candidates](actions/search-candidates.md) | `GET /c/:company_id/search/new/candidates` | [docs](https://docs.recruitee.com/reference/searchnewcandidates) |
| [Update Candidate](actions/update-candidate.md) | `PATCH /c/:company_id/candidates/:id` | [docs](https://docs.recruitee.com/reference/candidatesid-patch) |
| [Update Candidate Custom Fields](actions/update-candidate-custom-fields.md) | `POST /c/:company_id/custom_fields/candidates/:id/fields` | [docs](https://docs.recruitee.com/reference/custom_fieldscandidatesidfields-post) |
| [Update Candidate CV](actions/update-candidate-cv.md) | `PATCH /c/:company_id/candidates/:id/update_cv` | [docs](https://docs.recruitee.com/reference/candidatesidupdate_cv) |
| [Upload Attachment](actions/upload-attachment.md) | `POST /c/:company_id/attachments` | [docs](https://docs.recruitee.com/reference/attachments-post) |
