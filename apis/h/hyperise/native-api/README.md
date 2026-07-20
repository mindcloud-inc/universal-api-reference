# Hyperise: Native API Reference

A consolidated summary of Hyperise's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://hyperise.customerly.help/en/collections/4317-api
- **API base URL:** `https://app.hyperise.io/api/v1/regular`

## Authentication

### API Token

Use a Hyperise API token from Settings > API. MindCloud stores one token and sends it as the shared api_token query parameter.

### Credentials

- **API Token:** `apiKey` · required · Paste the Hyperise API token from Settings > API.

[Official authentication documentation](https://hyperise.customerly.help/en/articles/9936-Creating-API-token)

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Business](actions/create-business.md) | `POST /businesses` | [docs](https://hyperise.customerly.help/en/articles/9938-Prospect-Data-API) |
| [Create Organization](actions/create-organization.md) | `POST /organizations` | [docs](https://hyperise.customerly.help/en/articles/10000-create-client-account-api) |
| [Create Short Link](actions/create-short-link.md) | `POST /short-links` | [docs](https://hyperise.customerly.help/en/articles/9434-Personalised-Short-Links-API) |
| [Delete Business](actions/delete-business.md) | `DELETE /businesses/:businessId` | [docs](https://hyperise.customerly.help/en/articles/9938-Prospect-Data-API) |
| [Get Business](actions/get-business.md) | `GET /businesses/:businessId` | [docs](https://hyperise.customerly.help/en/articles/9938-Prospect-Data-API) |
| [Get Current User](actions/get-current-user.md) | `GET /users/current` | [docs](https://hyperise.customerly.help/en/articles/9940-User-Authentication-API) |
| [Get Enriched Prospect Data](actions/get-enriched-prospect-data.md) | `GET /data-enrichment` | [docs](https://hyperise.customerly.help/en/articles/9941-Data-Enrichment-API) |
| [List Businesses](actions/list-businesses.md) | `GET /businesses` | [docs](https://hyperise.customerly.help/en/articles/9938-Prospect-Data-API) |
| [List Image Templates](actions/list-image-templates.md) | `GET /image-templates` | [docs](https://hyperise.customerly.help/en/articles/9935-List-Image-Templates-API) |
| [List Image Views](actions/list-image-views.md) | `GET /image-impressions` | [docs](https://hyperise.customerly.help/en/articles/9939-Image-Views-API) |
| [List Short Links](actions/list-short-links.md) | `GET /short-links` | [docs](https://hyperise.customerly.help/en/articles/9434-Personalised-Short-Links-API) |
| [Update Business](actions/update-business.md) | `PUT /businesses/:businessId` | [docs](https://hyperise.customerly.help/en/articles/9938-Prospect-Data-API) |
