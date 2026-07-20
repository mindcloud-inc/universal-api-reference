# Toofr: Native API Reference

A consolidated summary of Toofr's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.findemails.com/?from=explinks.com
- **API base URL:** `https://www.findemails.com/api/v1`

## Authentication

### API Key

Use a Toofr/FindEmails API key. Requests send the secret as the provider parameter named key.

### Credentials

- **API Key:** `apiKey` · required · Your Toofr/FindEmails API key from the account page.

[Official authentication documentation](https://developer.findemails.com/?from=explinks.com)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Create Email List Records](actions/bulk-create-email-list-records.md) | `POST /lists/:list_id/list_records/bulk_list_records` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Classify Company](actions/classify-company.md) | `GET /classify` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Create Company Prospect List](actions/create-company-prospect-list.md) | `POST /lists` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Create Email List](actions/create-email-list.md) | `POST /lists` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Create Email List Record](actions/create-email-list-record.md) | `POST /lists/:list_id/list_records` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Create Email Pattern List](actions/create-email-pattern-list.md) | `POST /lists` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Create Email Verification List](actions/create-email-verification-list.md) | `POST /lists` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Create Guess All Processing List](actions/create-guess-all-processing-list.md) | `POST /lists` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Create Guess Processing List](actions/create-guess-processing-list.md) | `POST /lists` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Find Prospects](actions/find-prospects.md) | `GET /prospect` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Get Company Domain](actions/get-company-domain.md) | `GET /get_domain` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Get Company Prospects](actions/get-company-prospects.md) | `GET /get_prospects` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Get Email List](actions/get-email-list.md) | `GET /lists/:id` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Get Email List Record](actions/get-email-list-record.md) | `GET /lists/:list_id/list_records/:id` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Get Prospect Profile](actions/get-prospect-profile.md) | `GET /profile` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Guess Email](actions/guess-email.md) | `POST /guess_email.json` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [List Email List Records](actions/list-email-list-records.md) | `GET /lists/:list_id/list_records` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [List Marketplace Email Lists](actions/list-marketplace-email-lists.md) | `GET /lists` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [List Owned Email Lists](actions/list-owned-email-lists.md) | `GET /lists` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Purchase Marketplace List](actions/purchase-marketplace-list.md) | `POST /lists/:id/purchase` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Queue Email Guess](actions/queue-email-guess.md) | `POST /guess_email.json` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Search Marketplace Email Lists](actions/search-marketplace-email-lists.md) | `GET /lists/search` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Search Owned Email Lists](actions/search-owned-email-lists.md) | `GET /lists/search` | [docs](https://developer.findemails.com/?from=explinks.com) |
| [Verify Email](actions/verify-email.md) | `POST /test_email.json` | [docs](https://developer.findemails.com/?from=explinks.com) |
