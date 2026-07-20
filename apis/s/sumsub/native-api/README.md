# Sumsub: Native API Reference

A consolidated summary of Sumsub's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://docs.sumsub.com/reference
- **API base URL:** `https://api.sumsub.com`

## Authentication

### App token + secret key

Authenticate Sumsub API requests with an app token and a secret key. Requests must be signed per request using Sumsub's HMAC header contract.

### Credentials

- **App token:** `appToken` · required · App token generated in the Sumsub Dashboard under Dev space > App Tokens.

[Official authentication documentation](https://docs.sumsub.com/reference/authentication)

## API conventions

Response data is read from `list.items`.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Applicant Note](actions/add-applicant-note.md) | `POST /resources/api/applicants/notes` | [docs](https://docs.sumsub.com/reference/add-applicant-note) |
| [Add Applicant Tags](actions/add-applicant-tags.md) | `POST /resources/applicants/:applicantId/tags/add` | [docs](https://docs.sumsub.com/reference/add-custom-applicant-tags) |
| [Approve Applicant](actions/approve-applicant.md) | `POST /resources/applicants/:applicantId/-/approve` | [docs](https://docs.sumsub.com/reference/approve-applicant) |
| [Blocklist Applicant](actions/blocklist-applicant.md) | `POST /resources/applicants/:applicantId/blacklist` | [docs](https://docs.sumsub.com/reference/add-applicant-to-blocklist) |
| [Create Applicant](actions/create-applicant.md) | `POST /resources/applicants` | [docs](https://docs.sumsub.com/reference/create-applicant) |
| [Edit Applicant Note](actions/edit-applicant-note.md) | `PATCH /resources/api/applicants/notes` | [docs](https://docs.sumsub.com/reference/edit-applicant-note) |
| [Generate Access Token](actions/generate-access-token.md) | `POST /resources/accessTokens/sdk` | [docs](https://docs.sumsub.com/reference/generate-access-token) |
| [Get Applicant Data](actions/get-applicant-data.md) | `GET /resources/applicants/:applicantId/one` | [docs](https://docs.sumsub.com/reference/get-applicant-data) |
| [Get Applicant Data By External User ID](actions/get-applicant-data-by-external-user-id.md) | `GET /resources/applicants/-;externalUserId=:externalUserId/one` | [docs](https://docs.sumsub.com/reference/get-applicant-data-via-externaluserid) |
| [Get Applicant-Facing Consents](actions/get-applicant-facing-consents.md) | `GET /resources/applicants/:applicantId/acceptedAgreements` | [docs](https://docs.sumsub.com/reference/get-applicant-facing-consents) |
| [Get Applicant Review History](actions/get-applicant-review-history.md) | `GET /resources/applicants/:id/review/history` | [docs](https://docs.sumsub.com/reference/get-applicant-review-history) |
| [Get Applicant Review Status](actions/get-applicant-review-status.md) | `GET /resources/applicants/:applicantId/status` | [docs](https://docs.sumsub.com/reference/get-applicant-review-status) |
| [Get Document Image Metadata](actions/get-document-image-metadata.md) | `GET /resources/applicants/:applicantId/metadata/resources` | [docs](https://docs.sumsub.com/reference/get-information-about-document-images) |
| [Import Applicant From Archive](actions/import-applicant-from-archive.md) | `POST /resources/applicants/-/applicantImport` | [docs](https://docs.sumsub.com/reference/import-applicant-from-archive) |
| [List Applicant Actions](actions/list-applicant-actions.md) | `GET /resources/applicantActions/-;applicantId=:applicantId` | [docs](https://docs.sumsub.com/reference/get-applicant-actions) |
| [List Applicant Notes](actions/list-applicant-notes.md) | `GET /resources/api/applicants/notes` | [docs](https://docs.sumsub.com/reference/get-applicant-notes) |
| [List Verification Levels](actions/list-verification-levels.md) | `GET /resources/applicants/-/levels` | [docs](https://docs.sumsub.com/reference/levels-and-steps) |
