# Paperform: Native API Reference

A consolidated summary of Paperform's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://paperform.readme.io/reference/getting-started-1
- **API base URL:** `https://api.paperform.co/v1`

## Authentication

### Access Token

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://paperform.readme.io/reference/getting-started-1)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `results.forms`.

## Pagination

Use `limit` in the query string to set the page size (default 20). Use `skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Form](actions/get-form.md) | `GET /forms/:slug_or_id` | [docs](https://paperform.readme.io/reference/getform) |
| [Get Form Coupon](actions/get-form-coupon.md) | `GET /forms/:slug_or_id/coupons/:code` | [docs](https://paperform.readme.io/reference/getformcoupon) |
| [Get Form Field](actions/get-form-field.md) | `GET /forms/:slug_or_id/fields/:field_key` | [docs](https://paperform.readme.io/reference/getformfield) |
| [Get Form Partial Submission](actions/get-form-partial-submission.md) | `GET /forms/:slug_or_id/partial-submissions/:id` | [docs](https://paperform.readme.io/reference/getformpartialsubmission) |
| [Get Form Product](actions/get-form-product.md) | `GET /forms/:slug_or_id/products/:product_sku` | [docs](https://paperform.readme.io/reference/getformproduct) |
| [Get Form Submission](actions/get-form-submission.md) | `GET /forms/:slug_or_id/submissions/:id` | [docs](https://paperform.readme.io/reference/getformsubmission) |
| [Get Partial Submission](actions/get-partial-submission.md) | `GET /partial-submissions/:id` | [docs](https://paperform.readme.io/reference/getpartialsubmission) |
| [Get Submission](actions/get-submission.md) | `GET /submissions/:id` | [docs](https://paperform.readme.io/reference/getsubmission) |
| [List Form Coupons](actions/list-form-coupons.md) | `GET /forms/:slug_or_id/coupons` | [docs](https://paperform.readme.io/reference/listformcoupons) |
| [List Form Fields](actions/list-form-fields.md) | `GET /forms/:slug_or_id/fields` | [docs](https://paperform.readme.io/reference/listformfields) |
| [List Form Partial Submissions](actions/list-form-partial-submissions.md) | `GET /forms/:slug_or_id/partial-submissions` | [docs](https://paperform.readme.io/reference/listformpartialsubmissions) |
| [List Form Products](actions/list-form-products.md) | `GET /forms/:slug_or_id/products` | [docs](https://paperform.readme.io/reference/listformproducts) |
| [List Form Submissions](actions/list-form-submissions.md) | `GET /forms/:slug_or_id/submissions` | [docs](https://paperform.readme.io/reference/listformsubmissions) |
| [List Form Webhooks](actions/list-form-webhooks.md) | `GET /forms/:slug_or_id/webhooks` | [docs](https://paperform.readme.io/reference/listformwebhooks) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://paperform.readme.io/reference/listforms) |
