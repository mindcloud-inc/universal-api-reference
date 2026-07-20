# <img src="https://images.mindcloud.co/apps/icons/favicon-netlicensing-io-48x48-1_1777383029857.png" alt="NetLicensing logo" width="28" height="28"> NetLicensing: Universal API

NetLicensing is a license management and software monetization platform for managing products, licensees, licenses, tokens, transactions, bundles, and related licensing resources through a REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/netLicensing/latest
- **Actions:** 42
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://netlicensing.io
- **Vendor API docs:** https://netlicensing.io/wiki/restful-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (42)

### Bundle

| Action | Method | Description |
| --- | --- | --- |
| [Create Bundle](actions/create-bundle.md) | POST | Creates a new bundle in NetLicensing. |
| [Delete Bundle](actions/delete-bundle.md) | DELETE | Deletes an existing bundle from NetLicensing. |
| [Get Bundle](actions/get-bundle.md) | GET | Retrieves a bundle from NetLicensing. |
| [List Bundles](actions/list-bundles.md) | GET | Finds bundles in NetLicensing by filter criteria. |
| [Update Bundle](actions/update-bundle.md) | PUT | Updates an existing bundle in NetLicensing. |

### Bundle Obtainment

| Action | Method | Description |
| --- | --- | --- |
| [Obtain Bundle](actions/obtain-bundle.md) | POST | Creates licenses from a bundle in NetLicensing. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET |  |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET |  |

### License

| Action | Method | Description |
| --- | --- | --- |
| [Create License](actions/create-license.md) | POST | Creates a new license in NetLicensing. |
| [Delete License](actions/delete-license.md) | DELETE | Deletes an existing license from NetLicensing. |
| [Get License](actions/get-license.md) | GET | Retrieves a license from NetLicensing. |
| [List Licenses](actions/list-licenses.md) | GET | Finds licenses in NetLicensing by filter criteria. |
| [Update License](actions/update-license.md) | PUT | Updates an existing license in NetLicensing. |

### License Template

| Action | Method | Description |
| --- | --- | --- |
| [Get License Template](actions/get-license-template.md) | GET | Retrieves a license template from NetLicensing. |
| [List License Templates](actions/list-license-templates.md) | GET | Finds license templates in NetLicensing by filter criteria. |

### License Transfer

| Action | Method | Description |
| --- | --- | --- |
| [Transfer Licenses](actions/transfer-licenses.md) | PUT | Transfers licenses between licensees in NetLicensing. |

### License Type

| Action | Method | Description |
| --- | --- | --- |
| [List License Types](actions/list-license-types.md) | GET | Retrieves license types from NetLicensing. |

### Licensee

| Action | Method | Description |
| --- | --- | --- |
| [Create Licensee](actions/create-licensee.md) | POST | Creates a new licensee in NetLicensing. |
| [Delete Licensee](actions/delete-licensee.md) | DELETE | Deletes an existing licensee from NetLicensing. |
| [Get Licensee](actions/get-licensee.md) | GET | Retrieves a licensee from NetLicensing. |
| [List Licensees](actions/list-licensees.md) | GET | Finds licensees in NetLicensing by filter criteria. |
| [Update Licensee](actions/update-licensee.md) | PUT | Updates an existing licensee in NetLicensing. |

### Licensee Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Licensee](actions/validate-licensee.md) | GET | Retrieves license validation results from NetLicensing. |

### Licensing Model

| Action | Method | Description |
| --- | --- | --- |
| [List Licensing Models](actions/list-licensing-models.md) | GET | Retrieves licensing models from NetLicensing. |

### Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [Get Payment Method](actions/get-payment-method.md) | GET | Retrieves a payment method from NetLicensing. |
| [List Payment Methods](actions/list-payment-methods.md) | GET | Finds payment methods in NetLicensing by filter criteria. |
| [Update Payment Method](actions/update-payment-method.md) | PUT | Updates an existing payment method in NetLicensing. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in NetLicensing. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from NetLicensing. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from NetLicensing. |
| [List Products](actions/list-products.md) | GET | Finds products in NetLicensing by filter criteria. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in NetLicensing. |

### Product Module

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Module](actions/get-product-module.md) | GET | Retrieves a product module from NetLicensing. |
| [List Product Modules](actions/list-product-modules.md) | GET | Finds product modules in NetLicensing by filter criteria. |

### Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Token](actions/create-token.md) | POST | Creates a new token in NetLicensing. |
| [Delete Token](actions/delete-token.md) | DELETE | Deletes an existing token from NetLicensing. |
| [Get Token](actions/get-token.md) | GET | Retrieves a token from NetLicensing. |
| [List Tokens](actions/list-tokens.md) | GET | Finds tokens in NetLicensing by filter criteria. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Create Transaction](actions/create-transaction.md) | POST | Creates a new transaction in NetLicensing. |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from NetLicensing. |
| [List Transactions](actions/list-transactions.md) | GET | Finds transactions in NetLicensing by filter criteria. |
| [Update Transaction](actions/update-transaction.md) | PUT | Updates an existing transaction in NetLicensing. |

