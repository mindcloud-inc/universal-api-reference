# GoDaddy CRM: Native API Reference

A consolidated summary of GoDaddy CRM's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://developer.godaddy.com/doc
- **API base URL:** `https://api.godaddy.com`

## Authentication

### SSO Key

### Credentials

- **API Key:** `apiKey` · required · Your GoDaddy production API Key.
- **API Secret:** `apiSecret` · required · Your GoDaddy production Secret Key.

[Official authentication documentation](https://developer.godaddy.com/getstarted)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–250). Use `offset` in the query string as the record offset. Follow the complete next-page URL returned by the API.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add DNS Records](actions/add-dns-records.md) | `PATCH /v1/domains/:domain/records` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Cancel Subscription](actions/cancel-subscription.md) | `DELETE /v1/subscriptions/:subscriptionId` | [docs](https://developer.godaddy.com/doc/endpoint/subscriptions) |
| [Check Domain Availability](actions/check-domain-availability.md) | `GET /v1/domains/available` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Create Shopper Subaccount](actions/create-shopper-subaccount.md) | `POST /v1/shoppers/subaccount` | [docs](https://developer.godaddy.com/doc/endpoint/shoppers) |
| [Delete DNS Records By Type And Name](actions/delete-dns-records-by-type-and-name.md) | `DELETE /v1/domains/:domain/records/:type/:name` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Download Certificate](actions/download-certificate.md) | `GET /v2/certificates/download` | [docs](https://developer.godaddy.com/doc/endpoint/certificates) |
| [Get DNS Records](actions/get-dns-records.md) | `GET /v1/domains/:domain/records/:type/:name` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Get Domain Registration Schema](actions/get-domain-registration-schema.md) | `GET /v2/customers/:customerId/domains/register/schema/:tld` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Get Domain Transfer Status](actions/get-domain-transfer-status.md) | `GET /v2/customers/:customerId/domains/:domain/transfer` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Get Privacy Forwarding Settings](actions/get-privacy-forwarding-settings.md) | `GET /v2/customers/:customerId/domains/:domain/privacy/forwarding` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Get Shopper Details](actions/get-shopper-details.md) | `GET /v1/shoppers/:shopperId` | [docs](https://developer.godaddy.com/doc/endpoint/shoppers) |
| [Get Shopper Status](actions/get-shopper-status.md) | `GET /v1/shoppers/:shopperId/status` | [docs](https://developer.godaddy.com/doc/endpoint/shoppers) |
| [List Customer Certificates](actions/list-customer-certificates.md) | `GET /v2/customers/:customerId/certificates` | [docs](https://developer.godaddy.com/doc/endpoint/certificates) |
| [List Domain Actions](actions/list-domain-actions.md) | `GET /v2/customers/:customerId/domains/:domain/actions` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [List Domains](actions/list-domains.md) | `GET /v1/domains` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [List Orders](actions/list-orders.md) | `GET /v1/orders` | [docs](https://developer.godaddy.com/doc/endpoint/orders) |
| [List Subscription Product Groups](actions/list-subscription-product-groups.md) | `GET /v1/subscriptions/productGroups` | [docs](https://developer.godaddy.com/doc/endpoint/subscriptions) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /v1/subscriptions` | [docs](https://developer.godaddy.com/doc/endpoint/subscriptions) |
| [List Supported TLDs](actions/list-supported-tlds.md) | `GET /v1/domains/tlds` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Purchase Domain Privacy](actions/purchase-domain-privacy.md) | `POST /v1/domains/:domain/privacy/purchase` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Register Domain](actions/register-domain.md) | `POST /v2/customers/:customerId/domains/register` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Renew Domain](actions/renew-domain.md) | `POST /v2/customers/:customerId/domains/:domain/renew` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Replace All DNS Records](actions/replace-all-dns-records.md) | `PUT /v1/domains/:domain/records` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Replace Nameservers](actions/replace-nameservers.md) | `PUT /v2/customers/:customerId/domains/:domain/nameServers` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Retrieve Domain Details](actions/retrieve-domain-details.md) | `GET /v1/domains/:domain` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Retrieve Domain Purchase Agreements](actions/retrieve-domain-purchase-agreements.md) | `GET /v1/domains/agreements` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Retrieve Order Details](actions/retrieve-order-details.md) | `GET /v1/orders/:orderId` | [docs](https://developer.godaddy.com/doc/endpoint/orders) |
| [Retrieve Subscription Details](actions/retrieve-subscription-details.md) | `GET /v1/subscriptions/:subscriptionId` | [docs](https://developer.godaddy.com/doc/endpoint/subscriptions) |
| [Retry Domain Transfer In](actions/retry-domain-transfer-in.md) | `POST /v2/customers/:customerId/domains/:domain/transferInRetry` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Search Certificates](actions/search-certificates.md) | `GET /v2/certificates` | [docs](https://developer.godaddy.com/doc/endpoint/certificates) |
| [Start Domain Transfer In](actions/start-domain-transfer-in.md) | `POST /v2/customers/:customerId/domains/:domain/transfer` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Suggest Domains](actions/suggest-domains.md) | `GET /v1/domains/suggest` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Update Domain Contacts](actions/update-domain-contacts.md) | `PATCH /v2/customers/:customerId/domains/:domain/contacts` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Update Domain Details](actions/update-domain-details.md) | `PATCH /v1/domains/:domain` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Update Privacy Forwarding Settings](actions/update-privacy-forwarding-settings.md) | `PATCH /v2/customers/:customerId/domains/:domain/privacy/forwarding` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Update Shopper Details](actions/update-shopper-details.md) | `POST /v1/shoppers/:shopperId` | [docs](https://developer.godaddy.com/doc/endpoint/shoppers) |
| [Update Subscription](actions/update-subscription.md) | `PATCH /v1/subscriptions/:subscriptionId` | [docs](https://developer.godaddy.com/doc/endpoint/subscriptions) |
| [Validate Domain Registration](actions/validate-domain-registration.md) | `POST /v2/customers/:customerId/domains/register/validate` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
| [Validate Domain Transfer](actions/validate-domain-transfer.md) | `POST /v2/customers/:customerId/domains/:domain/transfer/validate` | [docs](https://developer.godaddy.com/doc/endpoint/domains) |
