# WeSupply: Native API Reference

A consolidated summary of WeSupply's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/11859344/T17AiAYq
- **API base URL:** `https://{subdomain}.labs.wesupply.xyz/api`

## Authentication

### OAuth 2.0 Client Credentials

Use WeSupply OAuth client credentials to mint a bearer token for tenant API access.

### Credentials

- **Subdomain:** `subdomain` · required · Your WeSupply client name or tenant subdomain, for example mindcloudstage0ws.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://{{credentials.subdomain}}.labs.wesupply.xyz/api/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `*`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://documenter.getpostman.com/view/11859344/T17AiAYq)

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Approve Return](actions/approve-return.md) | `POST /returns/flow/approval/execute` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#7bb2ff7a-8b80-4d47-bba9-5a3d9b6de866) |
| [Cancel Return](actions/cancel-return.md) | `POST /returns/flow/cancelation/execute` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#7bb2ff7a-8b80-4d47-bba9-5a3d9b6de866) |
| [Create Tracker](actions/create-tracker.md) | `POST /tracker/create` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#b3766a03-cffe-467a-80cb-b19af68bc5cb) |
| [Delete Customer Data](actions/delete-customer-data.md) | `POST /gdpr/delete` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#fa5b0e90-52c6-471d-8fa3-25fc906442d2) |
| [Get Customer Data](actions/get-customer-data.md) | `GET /gdpr/get` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#380c8688-b00d-498d-ae74-80b2fb35c552) |
| [Get Delivery Date Quotes](actions/get-delivery-date-quotes.md) | `GET /shippingQuotes` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#eb1fb1ec-b48a-4e17-961c-9b23e3372682) |
| [Get Estimated Delivery By Order ID](actions/get-estimated-delivery-by-order-id.md) | `POST /getEstimatedDeliveryByOrderId` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#a50a26e5-7690-42ce-90c7-f311c402ca2b) |
| [Get Order Links](actions/get-order-links.md) | `GET /authLinks` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#f0995f02-67c2-4909-bd67-b8681eb0ce65) |
| [Get Return By Customer Email](actions/get-return-by-customer-email.md) | `GET /returns/grabById` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#34a720b0-feb6-42f9-828a-b6912f00639b) |
| [Get Return By External Order ID](actions/get-return-by-external-order-id.md) | `GET /returns/grabById` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#af252121-fad4-481f-ab32-28d9318190e3) |
| [Get Return By Order ID](actions/get-return-by-order-id.md) | `GET /returns/grabById` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#66028da2-51d7-4a8d-ba24-8920c1bed478) |
| [Get Return By Reference](actions/get-return-by-reference.md) | `GET /returns/grabById` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#3856b919-635a-4965-a745-f3e8d9ced2a5) |
| [Get Shipping Estimate For One Product](actions/get-shipping-estimate-for-one-product.md) | `POST /shippingEstimate` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#983ca975-a4c2-43d8-82f1-f622397efeac) |
| [Get Shipping Estimates For Multiple Products](actions/get-shipping-estimates-for-multiple-products.md) | `POST /shippingEstimates` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#d465f074-9be3-43e8-9350-ed798bfad514) |
| [Import Orders](actions/import-orders.md) | `POST /json/import` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#63058bb9-87f1-4fac-8d89-51bd37b194d9) |
| [List Recent Returns](actions/list-recent-returns.md) | `GET /returns/recent` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#3bf52ef5-a33d-4a03-a65f-647422fd3283) |
| [List Returns By Page](actions/list-returns-by-page.md) | `GET /returns` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#b9964431-81ac-48e1-89d2-42b494eb6418) |
| [List Shipping Allowed Countries](actions/list-shipping-allowed-countries.md) | `GET /getShippingAllowedCountries` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#63d4b10a-55bd-403e-9bc8-787de2df4a0f) |
| [List Updated Item Details](actions/list-updated-item-details.md) | `GET /external/item-update` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#0d9b38f5-daf9-4cbd-a157-3a58e93cc9b0) |
| [Lookup Order By External Order ID](actions/lookup-order-by-external-order-id.md) | `GET /orders/lookup` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#e5cc24f3-c4e7-4daf-9f76-94753c120062) |
| [Lookup Order By Order ID](actions/lookup-order-by-order-id.md) | `GET /orders/lookup` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#e5cc24f3-c4e7-4daf-9f76-94753c120062) |
| [Lookup Orders By Customer Email](actions/lookup-orders-by-customer-email.md) | `GET /orders/lookup` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#e5cc24f3-c4e7-4daf-9f76-94753c120062) |
| [Quality Review Return](actions/quality-review-return.md) | `POST /returns/flow/quality/execute` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#7bb2ff7a-8b80-4d47-bba9-5a3d9b6de866) |
| [Refund Return](actions/refund-return.md) | `POST /returns/flow/refund/execute` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#7bb2ff7a-8b80-4d47-bba9-5a3d9b6de866) |
| [Subscribe To SMS Notifications](actions/subscribe-to-sms-notifications.md) | `GET /phone/v2/enrol` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#706fe420-d329-47ca-a056-e5400a52dcad) |
| [Unsubscribe From SMS Notifications](actions/unsubscribe-from-sms-notifications.md) | `GET /phone/v2/unsubscribe` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#e0f3c127-f724-4db2-a686-c09937b76a3a) |
| [Update Item Details](actions/update-item-details.md) | `POST /external/item-update` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#05e4d154-cc63-40cf-87ef-b95cd9529cac) |
| [Update Shipment](actions/update-shipment.md) | `POST /orders/shipment-update` | [docs](https://documenter.getpostman.com/view/11859344/T17AiAYq#60b62c7d-8aea-4b73-9cac-9b3725e71963) |
