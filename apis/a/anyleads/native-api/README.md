# Anyleads: Native API Reference

A consolidated summary of Anyleads's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://docs.anyleads.com/products/en
- **API base URL:** `https://myapiconnect.com`

## Authentication

### API Key

Custom auth for Anyleads webhook endpoints that require api_key in the JSON request body.

### Credentials

- **API Key:** `apiKey` · optional · Your Anyleads API key used in the webhook request body.

[Official authentication documentation](https://anyleads.com/products)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Domain Unsubscribe](actions/add-domain-unsubscribe.md) | `POST /api-product/incoming-webhook/add-domain-unsubscribe` | [docs](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool) |
| [Add Email Unsubscribe](actions/add-email-unsubscribe.md) | `POST /api-product/incoming-webhook/add-email-unsubscribe` | [docs](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool) |
| [Convert Company Names](actions/convert-company-names.md) | `POST /api-product/incoming-webhook/convert-company-names` | [docs](https://docs.anyleads.com/product/en/enrichment-data-software-to-find-emails) |
| [Create Contact](actions/create-contact.md) | `POST /api-product/incoming-webhook/create-a-contact` | [docs](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool) |
| [Enrich Company](actions/enrich-company.md) | `POST /api-product/incoming-webhook/enrich-company` | [docs](https://docs.anyleads.com/product/en/enrichment-data-software-to-find-emails) |
| [Extract Emails From URLs](actions/extract-emails-from-urls.md) | `POST /api-product/incoming-webhook/extract-emails-from-urls` | [docs](https://docs.anyleads.com/product/en/email-phone-social-media-extractor) |
| [Find Emails By Name And Domain](actions/find-emails-by-name-and-domain.md) | `POST /api-product/incoming-webhook/find-emails-first-last` | [docs](https://docs.anyleads.com/product/en/find-emails-from-first-name-last-name-and-company-name) |
| [Get Campaign Replies](actions/get-campaign-replies.md) | `POST /api-product/incoming-webhook/fetch-replies-from-single-campaign` | [docs](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool) |
| [Get Campaign Stats](actions/get-campaign-stats.md) | `POST /api-product/incoming-webhook/fetch-stats-from-single-campaign` | [docs](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool) |
| [Get Lead Replies](actions/get-lead-replies.md) | `POST /api-product/incoming-webhook/fetch-replies-from-single-lead` | [docs](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool) |
| [List Campaigns](actions/list-campaigns.md) | `POST /api-product/incoming-webhook/fetch-all-campaigns` | [docs](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool) |
| [Set Contact Converted](actions/set-contact-converted.md) | `POST /api-product/incoming-webhook/set-contact-converted` | [docs](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool) |
| [Stop Sending Email To Prospect](actions/stop-sending-email-to-prospect.md) | `POST /api-product/incoming-webhook/stop-sending-email-to-prospect` | [docs](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool) |
| [Update Contact](actions/update-contact.md) | `POST /api-product/incoming-webhook/update-a-contact` | [docs](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool) |
| [Update Contact Scoring](actions/update-contact-scoring.md) | `POST /api-product/incoming-webhook/update-a-contact-scoring` | [docs](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool) |
| [Verify Email State](actions/verify-email-state.md) | `POST /api-product/incoming-webhook/verify-email-state` | [docs](https://docs.anyleads.com/product/en/api-to-prevent-verify-emails-registration-on-your-service) |
