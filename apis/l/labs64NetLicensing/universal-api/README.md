# <img src="https://images.mindcloud.co/apps/icons/favicon-netlicensing-io-48x48_1776344631857.png" alt="Labs64 NetLicensing logo" width="28" height="28"> Labs64 NetLicensing: Universal API

Access the official Labs64 NetLicensing REST API for products, product modules, license templates, licensees, licenses, bundles, transactions, tokens, payment methods, and utility metadata.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/labs64NetLicensing/latest
- **Category:** Commerce
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://netlicensing.io
- **Vendor API docs:** https://netlicensing.io/wiki/restful-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Licensees](actions/list-licensees.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/labs64NetLicensing/latest/actions/list-licensees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Bundle

| Action | Method | Description |
| --- | --- | --- |
| [Create Bundle](actions/create-bundle.md) | POST |  |
| [Delete Bundle](actions/delete-bundle.md) | DELETE |  |
| [Get Bundle](actions/get-bundle.md) | GET |  |
| [List Bundles](actions/list-bundles.md) | GET |  |
| [Obtain Bundle](actions/obtain-bundle.md) | POST |  |
| [Update Bundle](actions/update-bundle.md) | PUT |  |

### License

| Action | Method | Description |
| --- | --- | --- |
| [Create License](actions/create-license.md) | POST |  |
| [Delete License](actions/delete-license.md) | DELETE |  |
| [Get License](actions/get-license.md) | GET |  |
| [List Licenses](actions/list-licenses.md) | GET |  |
| [Update License](actions/update-license.md) | PUT |  |

### License Template

| Action | Method | Description |
| --- | --- | --- |
| [Create License Template](actions/create-license-template.md) | POST |  |
| [Delete License Template](actions/delete-license-template.md) | DELETE |  |
| [Get License Template](actions/get-license-template.md) | GET |  |
| [List License Templates](actions/list-license-templates.md) | GET |  |
| [Update License Template](actions/update-license-template.md) | PUT |  |

### License Type

| Action | Method | Description |
| --- | --- | --- |
| [List License Types](actions/list-license-types.md) | GET |  |

### Licensee

| Action | Method | Description |
| --- | --- | --- |
| [Create Licensee](actions/create-licensee.md) | POST |  |
| [Delete Licensee](actions/delete-licensee.md) | DELETE |  |
| [Get Licensee](actions/get-licensee.md) | GET |  |
| [List Licensees](actions/list-licensees.md) | GET |  |
| [Transfer Licenses](actions/transfer-licenses.md) | PUT |  |
| [Update Licensee](actions/update-licensee.md) | PUT |  |
| [Validate Licensee](actions/validate-licensee.md) | GET |  |

### Licensing Model

| Action | Method | Description |
| --- | --- | --- |
| [List Licensing Models](actions/list-licensing-models.md) | GET |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [Delete Product](actions/delete-product.md) | DELETE |  |
| [Get Product](actions/get-product.md) | GET |  |
| [List Products](actions/list-products.md) | GET |  |
| [Update Product](actions/update-product.md) | PUT |  |

### Product Module

| Action | Method | Description |
| --- | --- | --- |
| [Create Product Module](actions/create-product-module.md) | POST |  |
| [Delete Product Module](actions/delete-product-module.md) | DELETE |  |
| [Get Product Module](actions/get-product-module.md) | GET |  |
| [List Product Modules](actions/list-product-modules.md) | GET |  |
| [Update Product Module](actions/update-product-module.md) | PUT |  |

