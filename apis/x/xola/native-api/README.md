# Xola: Native API Reference

A consolidated summary of Xola's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developers.xola.com/reference
- **API base URL:** `https://sandbox.xola.com/api`

## Authentication

### API Key

Authenticate Xola runtime requests with an application API key in the X-API-KEY header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://developers.xola.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Affiliate](actions/create-affiliate.md) | `POST /sellers/{id}/affiliates` | [docs](https://developers.xola.com/reference/create-an-affiliate) |
| [Create Button](actions/create-button.md) | `POST /buttons` | [docs](https://developers.xola.com/reference/create-a-button) |
| [Create Coupon](actions/create-coupon.md) | `POST /coupons` | [docs](https://developers.xola.com/reference/create-a-coupon) |
| [Create Event](actions/create-event.md) | `POST /events` | [docs](https://developers.xola.com/reference/create-an-event) |
| [Create Experience](actions/create-experience.md) | `POST /experiences` | [docs](https://developers.xola.com/reference/create-an-experience) |
| [Create Form](actions/create-form.md) | `POST /forms` | [docs](https://developers.xola.com/reference/create-a-form) |
| [Create Gift](actions/create-gift.md) | `POST /gifts` | [docs](https://developers.xola.com/reference/purchase-gift) |
| [Create Guide](actions/create-guide.md) | `POST /sellers/{id}/guides` | [docs](https://developers.xola.com/reference/create-a-guide) |
| [Create Package](actions/create-package.md) | `POST /packages` | [docs](https://developers.xola.com/reference/create-a-package) |
| [Get Batch Availability](actions/get-batch-availability.md) | `GET /availability` | [docs](https://developers.xola.com/reference/batch-availbility) |
| [Get Experience Availability](actions/get-experience-availability.md) | `GET /experiences/{id}/availability` | [docs](https://developers.xola.com/reference/experiencesidavailability) |
| [List Buttons](actions/list-buttons.md) | `GET /buttons` | [docs](https://developers.xola.com/reference/get-buttons) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://developers.xola.com/reference/categories) |
| [List Coupons](actions/list-coupons.md) | `GET /coupons` | [docs](https://developers.xola.com/reference/list-all-coupons) |
| [List Demographics](actions/list-demographics.md) | `GET /demographics` | [docs](https://developers.xola.com/reference/list-all-demographics) |
| [List Experiences](actions/list-experiences.md) | `GET /experiences` | [docs](https://developers.xola.com/reference/experiences) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://developers.xola.com/reference/list-all-forms) |
| [List Gifts](actions/list-gifts.md) | `GET /gifts` | [docs](https://developers.xola.com/reference/retrieve-a-list-of-gifts) |
| [List Guides](actions/list-guides.md) | `GET /sellers/{id}/guides` | [docs](https://developers.xola.com/reference/list-all-guides) |
| [List Packages](actions/list-packages.md) | `GET /packages` | [docs](https://developers.xola.com/reference/list-all-packages) |
| [List Transactions](actions/list-transactions.md) | `GET /transactions` | [docs](https://developers.xola.com/reference/list-transactions) |
| [Retrieve Button](actions/retrieve-button.md) | `GET /buttons/{id}` | [docs](https://developers.xola.com/reference/get-button) |
| [Retrieve Coupon](actions/retrieve-coupon.md) | `GET /coupons/{id}` | [docs](https://developers.xola.com/reference/retrieve-a-coupon) |
| [Retrieve Demographic](actions/retrieve-demographic.md) | `GET /demographics/{id}` | [docs](https://developers.xola.com/reference/retrieve-a-demographic) |
| [Retrieve Form](actions/retrieve-form.md) | `GET /forms/{id}` | [docs](https://developers.xola.com/reference/retrieve-a-form) |
| [Retrieve Order](actions/retrieve-order.md) | `GET /orders/{id}` | [docs](https://developers.xola.com/reference/retrieve-an-order) |
| [Retrieve Order Form](actions/retrieve-order-form.md) | `GET /orders/{id}/questions` | [docs](https://developers.xola.com/reference/retrieve-the-form-for-an-order) |
| [Retrieve Transaction](actions/retrieve-transaction.md) | `GET /transactions/{id}` | [docs](https://developers.xola.com/reference/retrieve-a-transansaction) |
| [Update Affiliate](actions/update-affiliate.md) | `PUT /sellers/{id}/affiliates` | [docs](https://developers.xola.com/reference/update-an-affiliate) |
| [Update Package](actions/update-package.md) | `PUT /packages/{id}` | [docs](https://developers.xola.com/reference/r-create-a-package-copy) |
