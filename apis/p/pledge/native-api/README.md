# Pledge: Native API Reference

A consolidated summary of Pledge's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://developer.pledge.to/api/
- **OpenAPI specification:** https://developer.pledge.to/api.yaml
- **API base URL:** `https://api.pledge.to/v1`

## Authentication

### API Key

Authenticate with a Pledge API key from Impact Hub.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.pledge.to/guides/getting-started/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `page`.

## Pagination

Use `per` in the query string to set the page size (default 25). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Donation](actions/create-donation.md) | `POST /donations` | [docs](https://developer.pledge.to/api/#tag/Donations/operation/createDonation) |
| [Create Fundraiser](actions/create-fundraiser.md) | `POST /fundraisers` | [docs](https://developer.pledge.to/api/#tag/Fundraisers/operation/createFundraiser) |
| [Create Impact Calculator](actions/create-impact-calculator.md) | `POST /impact_calculators` | [docs](https://developer.pledge.to/api/#tag/Impact%20Calculators/operation/createImpactCalculator) |
| [Create Webhook Endpoint](actions/create-webhook-endpoint.md) | `POST /webhooks` | [docs](https://developer.pledge.to/api/#tag/Webhook%20Endpoints/operation/createWebhookEndpoint) |
| [Delete Webhook Endpoint](actions/delete-webhook-endpoint.md) | `DELETE /webhooks/[:id]` | [docs](https://developer.pledge.to/api/#tag/Webhook%20Endpoints/operation/deleteWebhookEndpoint) |
| [Get Donation](actions/get-donation.md) | `GET /donations/[:id]` | [docs](https://developer.pledge.to/api/#tag/Donations/operation/getDonation) |
| [Get Fundraiser](actions/get-fundraiser.md) | `GET /fundraisers/[:id]` | [docs](https://developer.pledge.to/api/#tag/Fundraisers/operation/getFundraiser) |
| [Get Impact Calculator](actions/get-impact-calculator.md) | `GET /impact_calculators/[:id]` | [docs](https://developer.pledge.to/api/#tag/Impact%20Calculators/operation/getImpactCalculator) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/[:id]` | [docs](https://developer.pledge.to/api/#tag/Organizations/operation/getOrganization) |
| [Get Webhook Endpoint](actions/get-webhook-endpoint.md) | `GET /webhooks/[:id]` | [docs](https://developer.pledge.to/api/#tag/Webhook%20Endpoints/operation/getWebhookEndpoint) |
| [List Donations](actions/list-donations.md) | `GET /donations` | [docs](https://developer.pledge.to/api/#tag/Donations/operation/getAllDonations) |
| [List Impact Calculators](actions/list-impact-calculators.md) | `GET /impact_calculators` | [docs](https://developer.pledge.to/api/#tag/Impact%20Calculators/operation/getAllImpactCalculators) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://developer.pledge.to/api/#tag/Organizations/operation/getAllOrganizations) |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | `GET /webhooks` | [docs](https://developer.pledge.to/api/#tag/Webhook%20Endpoints/operation/getAllWebhookEndpoints) |
| [Place Fundraiser](actions/place-fundraiser.md) | `PUT /fundraisers/[:id]` | [docs](https://developer.pledge.to/api/#tag/Fundraisers/operation/placeFundraiser) |
| [Request Organization](actions/request-organization.md) | `POST /organizations` | [docs](https://developer.pledge.to/api/#tag/Organizations/operation/requestOrganization) |
| [Update Fundraiser](actions/update-fundraiser.md) | `PATCH /fundraisers/[:id]` | [docs](https://developer.pledge.to/api/#tag/Fundraisers/operation/updateFundraiser) |
| [Update Impact Calculator](actions/update-impact-calculator.md) | `PATCH /impact_calculators/[:id]` | [docs](https://developer.pledge.to/api/#tag/Impact%20Calculators/operation/updateImpactCalculator) |
