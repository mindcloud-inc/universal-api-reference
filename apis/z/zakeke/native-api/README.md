# Zakeke: Native API Reference

A consolidated summary of Zakeke's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://docs.zakeke.com/docs/API/Introduction-API
- **API base URL:** `https://api.zakeke.com`

## Authentication

### OAuth 2.0 (Client Credentials)

Zakeke uses OAuth 2.0 client credentials to obtain S2S bearer tokens for API calls.

### Credentials

- **Client ID:** `clientId` · required · Your Zakeke API client ID from Your Account > API keys.
- **Client Secret:** `clientSecret` · required · Your Zakeke API client secret from Your Account > API keys.
- **Customer Code:** `customerCode` · optional · Optional ecommerce customer identifier for S2S tokens used by endpoints such as order registration.
- **Visitor Code:** `visitorCode` · optional · Optional ecommerce visitor identifier for S2S tokens used by endpoints such as order registration.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.zakeke.com/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.zakeke.com/docs/API/authentication-and-authorization)

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Import Status](actions/check-import-status.md) | `GET /v2/csv/importingresult/:taskID` | [docs](https://api-reference.zakeke.com/docs) |
| [Count Designs](actions/count-designs.md) | `GET /v1/designs/seller/occurrences` | [docs](https://docs.zakeke.com/docs/API/designs-API#10-total-number-of-designs) |
| [Delete Templates By Code](actions/delete-templates-by-code.md) | `POST /v1/designs/templates/code/:templateCode/delete` | [docs](https://docs.zakeke.com/docs/API/designs-API#12-delete-templates-by-code) |
| [Duplicate Design](actions/duplicate-design.md) | `POST /v2/designs/{designID}` | [docs](https://docs.zakeke.com/docs/API/designs-API#5-duplicate-a-design) |
| [Import Products Via CSV](actions/import-products-via-csv.md) | `POST /v2/csv/import` | [docs](https://docs.zakeke.com/docs/API/Integration/Connecting-Product/CSV-method#2-first-step-upload-the-csv-zip-file) |
| [Import Provider Product Templates](actions/import-provider-product-templates.md) | `POST /v2/providerproducts/importTemplates` | [docs](https://api-reference.zakeke.com/docs) |
| [Import Provider Products](actions/import-provider-products.md) | `POST /v2/providerproducts/import` | [docs](https://docs.zakeke.com/docs/API/Integration/Connecting-Product/CSV-method#3-second-step-check-the-import-status) |
| [List Customers Who Created Compositions](actions/list-customers-who-created-compositions.md) | `GET /v2/compositions/seller/customers` | [docs](https://docs.zakeke.com/docs/API/compositions-API#7-customers-who-created-compositions) |
| [List Customers Who Created Designs](actions/list-customers-who-created-designs.md) | `GET /v1/designs/seller/customers` | [docs](https://docs.zakeke.com/docs/API/designs-API#11-customers-who-created-designs) |
| [Register Order](actions/register-order.md) | `POST /v2/order` | [docs](https://docs.zakeke.com/docs/API/orders-API#7-register-an-order) |
| [Register Webhook](actions/register-webhook.md) | `POST /v2/webhook` | [docs](https://api-reference.zakeke.com/docs) |
| [Retrieve Composition By ID](actions/retrieve-composition-by-id.md) | `GET /v2/compositions/{compositionID}/{quantity}` | [docs](https://docs.zakeke.com/docs/API/compositions-API#4-retrieve-a-composition-by-id) |
| [Retrieve Composition Cart Info](actions/retrieve-composition-cart-info.md) | `GET /v2/compositions/{id}/cartinfo` | [docs](https://docs.zakeke.com/docs/API/compositions-API#5-get-the-necessary-data-to-add-a-configured-product-to-the-shopping-cart) |
| [Retrieve Design By ID](actions/retrieve-design-by-id.md) | `GET /v3/designs/{designID}/{quantity}` | [docs](https://docs.zakeke.com/docs/API/designs-API#4-retrieve-a-design-by-id) |
| [Retrieve Design Items](actions/retrieve-design-items.md) | `GET /v1/designs/{designID}/items` | [docs](https://docs.zakeke.com/docs/API/designs-API#6-retrieve-design-items) |
| [Retrieve Order By Code](actions/retrieve-order-by-code.md) | `GET /v2/order/{orderCode}` | [docs](https://docs.zakeke.com/docs/API/orders-API#5-retrieve-an-order-by-code) |
| [Retrieve Order By ID](actions/retrieve-order-by-id.md) | `GET /v2/orders/{order}` | [docs](https://docs.zakeke.com/docs/API/orders-API#6-retrieve-an-order-by-id) |
| [Retrieve Print-Ready File](actions/retrieve-print-ready-file.md) | `GET /v1/designs/{designID}/outputfiles/{fileFormat}` | [docs](https://docs.zakeke.com/docs/API/designs-API#8-retrieve-print-ready-file-with-a-given-file-format) |
| [Retrieve Print-Ready ZIP](actions/retrieve-print-ready-zip.md) | `GET /v1/designs/{designID}/outputfiles/zip` | [docs](https://docs.zakeke.com/docs/API/designs-API#7-retrieve-the-zip-with-all-print-ready-files) |
| [Retrieve Seller Setup Status](actions/retrieve-seller-setup-status.md) | `GET /v2/sellerSetupStatus` | [docs](https://api-reference.zakeke.com/docs) |
| [Update Provider Products](actions/update-provider-products.md) | `POST /v2/providerproducts/update` | [docs](https://api-reference.zakeke.com/docs) |
