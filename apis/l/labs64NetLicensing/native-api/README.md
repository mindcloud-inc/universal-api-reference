# Labs64 NetLicensing: Native API Reference

A consolidated summary of Labs64 NetLicensing's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://netlicensing.io/wiki/restful-api
- **API base URL:** `https://go.netlicensing.io/core/v2/rest`

## Authentication

### Basic Authentication

Authenticate NetLicensing REST requests with HTTP Basic auth. Use the fixed username `apiKey` and your NetLicensing API key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
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

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bundle](actions/create-bundle.md) | `POST /bundle` | [docs](https://netlicensing.io/wiki/bundle-services) |
| [Create License](actions/create-license.md) | `POST /license` | [docs](https://netlicensing.io/wiki/license-services) |
| [Create License Template](actions/create-license-template.md) | `POST /licensetemplate` | [docs](https://netlicensing.io/wiki/license-template-services) |
| [Create Licensee](actions/create-licensee.md) | `POST /licensee` | [docs](https://netlicensing.io/wiki/licensee-services) |
| [Create Product](actions/create-product.md) | `POST /product` | [docs](https://netlicensing.io/wiki/product-services) |
| [Create Product Module](actions/create-product-module.md) | `POST /productmodule` | [docs](https://netlicensing.io/wiki/product-module-services) |
| [Delete Bundle](actions/delete-bundle.md) | `DELETE /bundle/{bundleNumber}` | [docs](https://netlicensing.io/wiki/bundle-services) |
| [Delete License](actions/delete-license.md) | `DELETE /license/{licenseNumber}` | [docs](https://netlicensing.io/wiki/license-services) |
| [Delete License Template](actions/delete-license-template.md) | `DELETE /licensetemplate/{licenseTemplateNumber}` | [docs](https://netlicensing.io/wiki/license-template-services) |
| [Delete Licensee](actions/delete-licensee.md) | `DELETE /licensee/{licenseeNumber}` | [docs](https://netlicensing.io/wiki/licensee-services) |
| [Delete Product](actions/delete-product.md) | `DELETE /product/{productNumber}` | [docs](https://netlicensing.io/wiki/product-services) |
| [Delete Product Module](actions/delete-product-module.md) | `DELETE /productmodule/{productModuleNumber}` | [docs](https://netlicensing.io/wiki/product-module-services) |
| [Get Bundle](actions/get-bundle.md) | `GET /bundle/{bundleNumber}` | [docs](https://netlicensing.io/wiki/bundle-services) |
| [Get License](actions/get-license.md) | `GET /license/{licenseNumber}` | [docs](https://netlicensing.io/wiki/license-services) |
| [Get License Template](actions/get-license-template.md) | `GET /licensetemplate/{licenseTemplateNumber}` | [docs](https://netlicensing.io/wiki/license-template-services) |
| [Get Licensee](actions/get-licensee.md) | `GET /licensee/{licenseeNumber}` | [docs](https://netlicensing.io/wiki/licensee-services) |
| [Get Product](actions/get-product.md) | `GET /product/{productNumber}` | [docs](https://netlicensing.io/wiki/product-services) |
| [Get Product Module](actions/get-product-module.md) | `GET /productmodule/{productModuleNumber}` | [docs](https://netlicensing.io/wiki/product-module-services) |
| [List Bundles](actions/list-bundles.md) | `GET /bundle` | [docs](https://netlicensing.io/wiki/bundle-services) |
| [List License Templates](actions/list-license-templates.md) | `GET /licensetemplate` | [docs](https://netlicensing.io/wiki/license-template-services) |
| [List License Types](actions/list-license-types.md) | `GET /utility/licenseTypes` | [docs](https://netlicensing.io/wiki/utility-services) |
| [List Licensees](actions/list-licensees.md) | `GET /licensee` | [docs](https://netlicensing.io/wiki/licensee-services) |
| [List Licenses](actions/list-licenses.md) | `GET /license` | [docs](https://netlicensing.io/wiki/license-services) |
| [List Licensing Models](actions/list-licensing-models.md) | `GET /utility/licensingModels` | [docs](https://netlicensing.io/wiki/utility-services) |
| [List Product Modules](actions/list-product-modules.md) | `GET /productmodule` | [docs](https://netlicensing.io/wiki/product-module-services) |
| [List Products](actions/list-products.md) | `GET /product` | [docs](https://netlicensing.io/wiki/product-services) |
| [Obtain Bundle](actions/obtain-bundle.md) | `POST /bundle/{bundleNumber}/obtain` | [docs](https://netlicensing.io/wiki/bundle-services) |
| [Transfer Licenses](actions/transfer-licenses.md) | `POST /licensee/{licenseeNumber}/transfer` | [docs](https://netlicensing.io/wiki/licensee-services) |
| [Update Bundle](actions/update-bundle.md) | `POST /bundle/{bundleNumber}` | [docs](https://netlicensing.io/wiki/bundle-services) |
| [Update License](actions/update-license.md) | `POST /license/{licenseNumber}` | [docs](https://netlicensing.io/wiki/license-services) |
| [Update License Template](actions/update-license-template.md) | `POST /licensetemplate/{licenseTemplateNumber}` | [docs](https://netlicensing.io/wiki/license-template-services) |
| [Update Licensee](actions/update-licensee.md) | `POST /licensee/{licenseeNumber}` | [docs](https://netlicensing.io/wiki/licensee-services) |
| [Update Product](actions/update-product.md) | `POST /product/{productNumber}` | [docs](https://netlicensing.io/wiki/product-services) |
| [Update Product Module](actions/update-product-module.md) | `POST /productmodule/{productModuleNumber}` | [docs](https://netlicensing.io/wiki/product-module-services) |
| [Validate Licensee](actions/validate-licensee.md) | `POST /licensee/{licenseeNumber}/validate` | [docs](https://netlicensing.io/wiki/licensee-services) |
