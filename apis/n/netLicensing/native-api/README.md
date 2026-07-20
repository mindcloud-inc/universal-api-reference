# NetLicensing: Native API Reference

A consolidated summary of NetLicensing's API configuration and 42 documented operations, with links to official documentation.

- **Official docs:** https://netlicensing.io/wiki/restful-api
- **API base URL:** `https://go.netlicensing.io/core/v2/rest`

## Authentication

### API Key

Use NetLicensing API Key Identification. NetLicensing requires HTTP Basic authentication with username `apiKey` and the API key as the password.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://netlicensing.io/wiki/security)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON. Response data is read from `items.item`.

## Retry behavior

Retry responses with status codes `408,429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (42 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bundle](actions/create-bundle.md) | `POST /bundle` | [docs](https://netlicensing.io/wiki/bundle-services) |
| [Create License](actions/create-license.md) | `POST /license` | [docs](https://netlicensing.io/wiki/license-services) |
| [Create Licensee](actions/create-licensee.md) | `POST /licensee` | [docs](https://netlicensing.io/wiki/licensee-services) |
| [Create Product](actions/create-product.md) | `POST /product` | [docs](https://netlicensing.io/wiki/product-services) |
| [Create Token](actions/create-token.md) | `POST /token` | [docs](https://netlicensing.io/wiki/token-services) |
| [Create Transaction](actions/create-transaction.md) | `POST /transaction` | [docs](https://netlicensing.io/wiki/transaction-services) |
| [Delete Bundle](actions/delete-bundle.md) | `DELETE /bundle/{bundleNumber}` | [docs](https://netlicensing.io/wiki/bundle-services) |
| [Delete License](actions/delete-license.md) | `DELETE /license/{licenseNumber}` | [docs](https://netlicensing.io/wiki/license-services) |
| [Delete Licensee](actions/delete-licensee.md) | `DELETE /licensee/{licenseeNumber}` | [docs](https://netlicensing.io/wiki/licensee-services) |
| [Delete Product](actions/delete-product.md) | `DELETE /product/{productNumber}` | [docs](https://netlicensing.io/wiki/product-services) |
| [Delete Token](actions/delete-token.md) | `DELETE /token/{tokenNumber}` | [docs](https://netlicensing.io/wiki/token-services) |
| [Get Bundle](actions/get-bundle.md) | `GET /bundle/{bundleNumber}` | [docs](https://netlicensing.io/wiki/bundle-services) |
| [Get License](actions/get-license.md) | `GET /license/{licenseNumber}` | [docs](https://netlicensing.io/wiki/license-services) |
| [Get License Template](actions/get-license-template.md) | `GET /licensetemplate/{licenseTemplateNumber}` | [docs](https://netlicensing.io/wiki/license-template-services) |
| [Get Licensee](actions/get-licensee.md) | `GET /licensee/{licenseeNumber}` | [docs](https://netlicensing.io/wiki/licensee-services) |
| [Get Payment Method](actions/get-payment-method.md) | `GET /paymentmethod/{paymentMethodNumber}` | [docs](https://netlicensing.io/wiki/payment-method-services) |
| [Get Product](actions/get-product.md) | `GET /product/{productNumber}` | [docs](https://netlicensing.io/wiki/product-services) |
| [Get Product Module](actions/get-product-module.md) | `GET /productmodule/{productModuleNumber}` | [docs](https://netlicensing.io/wiki/product-module-services) |
| [Get Token](actions/get-token.md) | `GET /token/{tokenNumber}` | [docs](https://netlicensing.io/wiki/token-services) |
| [Get Transaction](actions/get-transaction.md) | `GET /transaction/{transactionNumber}` | [docs](https://netlicensing.io/wiki/transaction-services) |
| [List Bundles](actions/list-bundles.md) | `GET /bundle` | [docs](https://netlicensing.io/wiki/bundle-services) |
| [List Countries](actions/list-countries.md) | `GET /utility/countries` | [docs](https://netlicensing.io/wiki/utility-services) |
| [List Currencies](actions/list-currencies.md) | `GET /utility/currencies` | [docs](https://netlicensing.io/wiki/utility-services) |
| [List License Templates](actions/list-license-templates.md) | `GET /licensetemplate` | [docs](https://netlicensing.io/wiki/license-template-services) |
| [List License Types](actions/list-license-types.md) | `GET /utility/licenseTypes` | [docs](https://netlicensing.io/wiki/utility-services) |
| [List Licensees](actions/list-licensees.md) | `GET /licensee` | [docs](https://netlicensing.io/wiki/licensee-services) |
| [List Licenses](actions/list-licenses.md) | `GET /license` | [docs](https://netlicensing.io/wiki/license-services) |
| [List Licensing Models](actions/list-licensing-models.md) | `GET /utility/licensingModels` | [docs](https://netlicensing.io/wiki/utility-services) |
| [List Payment Methods](actions/list-payment-methods.md) | `GET /paymentmethod` | [docs](https://netlicensing.io/wiki/payment-method-services) |
| [List Product Modules](actions/list-product-modules.md) | `GET /productmodule` | [docs](https://netlicensing.io/wiki/product-module-services) |
| [List Products](actions/list-products.md) | `GET /product` | [docs](https://netlicensing.io/wiki/product-services) |
| [List Tokens](actions/list-tokens.md) | `GET /token` | [docs](https://netlicensing.io/wiki/token-services) |
| [List Transactions](actions/list-transactions.md) | `GET /transaction` | [docs](https://netlicensing.io/wiki/transaction-services) |
| [Obtain Bundle](actions/obtain-bundle.md) | `POST /bundle/{bundleNumber}/obtain` | [docs](https://netlicensing.io/wiki/bundle-services) |
| [Transfer Licenses](actions/transfer-licenses.md) | `POST /licensee/{licenseeNumber}/transfer` | [docs](https://netlicensing.io/wiki/licensee-services) |
| [Update Bundle](actions/update-bundle.md) | `POST /bundle/{bundleNumber}` | [docs](https://netlicensing.io/wiki/bundle-services) |
| [Update License](actions/update-license.md) | `POST /license/{licenseNumber}` | [docs](https://netlicensing.io/wiki/license-services) |
| [Update Licensee](actions/update-licensee.md) | `POST /licensee/{licenseeNumber}` | [docs](https://netlicensing.io/wiki/licensee-services) |
| [Update Payment Method](actions/update-payment-method.md) | `POST /paymentmethod/{paymentMethodNumber}` | [docs](https://netlicensing.io/wiki/payment-method-services) |
| [Update Product](actions/update-product.md) | `POST /product/{productNumber}` | [docs](https://netlicensing.io/wiki/product-services) |
| [Update Transaction](actions/update-transaction.md) | `POST /transaction/{transactionNumber}` | [docs](https://netlicensing.io/wiki/transaction-services) |
| [Validate Licensee](actions/validate-licensee.md) | `POST /licensee/{licenseeNumber}/validate` | [docs](https://netlicensing.io/wiki/licensee-services) |
