# Sertifier: Native API Reference

A consolidated summary of Sertifier's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://sertifier.docs.apiary.io
- **API base URL:** `https://b2b.sertifier.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
secretKey: <apiKey>
```

[Official authentication documentation](https://help.sertifier.com/where-can-i-find-my-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `api-version` | `3.3` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `length` in the request body to set the page size (default 10). Use `startIndex` in the request body as the record offset; numbering starts at 0.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Attribute](actions/add-attribute.md) | `POST /attribute` | [docs](https://sertifier.docs.apiary.io/reference/attribute/add-attribute) |
| [Add Campaign](actions/add-campaign.md) | `POST /campaign` | [docs](https://sertifier.docs.apiary.io/reference/campaign/add-campaign) |
| [Add Credentials To Campaign](actions/add-credentials-to-campaign.md) | `POST /campaign/addCredentials` | [docs](https://sertifier.docs.apiary.io/reference/campaign/add-credentials) |
| [Add Recipient](actions/add-recipient.md) | `POST /recipient` | [docs](https://sertifier.docs.apiary.io/reference/recipient/add-update-recipient) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE /campaign/:campaign_id` | [docs](https://sertifier.docs.apiary.io/reference/campaign/get-update-delete-campaign) |
| [Delete Credential](actions/delete-credential.md) | `DELETE /credential/:credential_id` | [docs](https://sertifier.docs.apiary.io/reference/credential/get-update-delete-credential) |
| [Delete Recipient](actions/delete-recipient.md) | `DELETE /recipient/:recipient_id` | [docs](https://sertifier.docs.apiary.io/reference/recipient/delete-recipient) |
| [Generate Credential PDF Link](actions/generate-credential-pdf-link.md) | `GET /credential/generatePDFLink/:credential_id_OR_certificate_no` | [docs](https://sertifier.docs.apiary.io/reference/credential/generate-pdf-download-link-of-credential) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaign/:campaign_id` | [docs](https://sertifier.docs.apiary.io/reference/campaign/get-update-delete-campaign) |
| [Get Credential](actions/get-credential.md) | `GET /credential/:credential_id` | [docs](https://sertifier.docs.apiary.io/reference/credential/get-update-delete-credential) |
| [List Attributes](actions/list-attributes.md) | `POST /attribute/search` | [docs](https://sertifier.docs.apiary.io/reference/attribute/search-attributes) |
| [List Campaigns](actions/list-campaigns.md) | `POST /campaign/search` | [docs](https://sertifier.docs.apiary.io/reference/campaign/search-campaigns) |
| [List Credentials](actions/list-credentials.md) | `POST /credential/search` | [docs](https://sertifier.docs.apiary.io/reference/credential/search-credentials) |
| [List Recipients](actions/list-recipients.md) | `POST /recipient/search` | [docs](https://sertifier.docs.apiary.io/reference/recipient/search-recipients) |
| [List Skills](actions/list-skills.md) | `POST /detail/searchSkills` | [docs](https://sertifier.docs.apiary.io/reference/detail/search-skills) |
| [Publish Credential](actions/publish-credential.md) | `POST /credential/publish` | [docs](https://sertifier.docs.apiary.io/reference/credential/publish-credential) |
| [Schedule Campaign](actions/schedule-campaign.md) | `POST /campaign/schedule` | [docs](https://sertifier.docs.apiary.io/reference/campaign/schedule) |
| [Send Campaign](actions/send-campaign.md) | `POST /campaign/send` | [docs](https://sertifier.docs.apiary.io/reference/campaign/send) |
| [Test Authentication](actions/test-authentication.md) | `GET /Test` | [docs](https://sertifier.docs.apiary.io/reference/test/test) |
| [Update Attribute](actions/update-attribute.md) | `PUT /attribute/:attributeId` | [docs](https://sertifier.docs.apiary.io/reference/attribute/update-delete-attribute) |
| [Update Campaign](actions/update-campaign.md) | `PUT /campaign/:campaign_id` | [docs](https://sertifier.docs.apiary.io/reference/campaign/get-update-delete-campaign) |
| [Update Credential](actions/update-credential.md) | `PUT /credential/:credential_id` | [docs](https://sertifier.docs.apiary.io/reference/credential/get-update-delete-credential) |
| [Update Recipient](actions/update-recipient.md) | `PUT /recipient` | [docs](https://sertifier.docs.apiary.io/reference/recipient/add-update-recipient) |
