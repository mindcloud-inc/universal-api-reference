# DigiCert: Native API Reference

A consolidated summary of DigiCert's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://dev.digicert.com/certcentral-apis/services-api.html
- **API base URL:** `https://www.digicert.com/services/v2`

## Authentication

### DigiCert API Key

Use a DigiCert CertCentral Services API key. DigiCert Services API requests send the key in the X-DC-DEVKEY header.

### Credentials

- **API Key:** `apiKey` · required · Your DigiCert CertCentral Services API key. DigiCert sends it in the X-DC-DEVKEY header on every request.

Send these headers with each API request:

```http
X-DC-DEVKEY: <apiKey>
```

[Official authentication documentation](https://dev.digicert.com/certcentral-apis/services-api.html)

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Permission](actions/check-permission.md) | `GET /authorization/:permission` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [Get Account Details](actions/get-account-details.md) | `GET /account` | [docs](https://dev.digicert.com/services-api/account/account-details) |
| [Get API Key Details](actions/get-api-key-details.md) | `GET /key/:api_key_id` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [Get Auth Key Details](actions/get-auth-key-details.md) | `GET /account/auth-key/:auth_key_id` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [Get Container Details](actions/get-container-details.md) | `GET /container/:container_id` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [Get Contract Details](actions/get-contract-details.md) | `GET /account/contract` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [Get Domain Details](actions/get-domain-details.md) | `GET /domain/:domain_id` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [Get Domain Validation Details](actions/get-domain-validation-details.md) | `GET /domain/:domain_id/validation` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [Get Domain Validation Types](actions/get-domain-validation-types.md) | `GET /domain/validation/type` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [Get Order Details](actions/get-order-details.md) | `GET /order/certificate/:order_id` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [Get Order Validation Status](actions/get-order-validation-status.md) | `GET /order/certificate/:order_id/validation` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [Get Organization Details](actions/get-organization-details.md) | `GET /organization/:organization_id` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [Get Organization Validation Details](actions/get-organization-validation-details.md) | `GET /organization/:organization_id/validation` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [Get Product Details](actions/get-product-details.md) | `GET /product/:product_id` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [Get Subaccount Details](actions/get-subaccount-details.md) | `GET /account/subaccount/:subaccount_id` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [Get User Details](actions/get-user-details.md) | `GET /user/:user_id` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [Get Webhook Event Logs](actions/get-webhook-event-logs.md) | `GET /webhook/:webhook_id/event-logs` | [docs](https://dev.digicert.com/en/certcentral-apis/services-api/webhooks/webhook-event-logs.html) |
| [List API Keys](actions/list-api-keys.md) | `GET /key` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [List Auth Keys](actions/list-auth-keys.md) | `GET /account/auth-keys` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [List Containers](actions/list-containers.md) | `GET /container` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [List Domain DCV Methods](actions/list-domain-dcv-methods.md) | `GET /domain/:domain_id/dcv/method` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [List Domains](actions/list-domains.md) | `GET /domain` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [List Duplicates](actions/list-duplicates.md) | `GET /order/certificate/:order_id/duplicate` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [List Order Notes](actions/list-order-notes.md) | `GET /order/certificate/:order_id/note` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [List Orders](actions/list-orders.md) | `GET /order/certificate` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [List Organization Approvers](actions/list-organization-approvers.md) | `GET /organization/potential-approvers` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [List Organizations](actions/list-organizations.md) | `GET /organization` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [List Permissions](actions/list-permissions.md) | `GET /authorization` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [List Pricing](actions/list-pricing.md) | `GET /product/pricing` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [List Products](actions/list-products.md) | `GET /product` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [List Reissues](actions/list-reissues.md) | `GET /order/certificate/:order_id/reissue` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [List Service Users](actions/list-service-users.md) | `GET /user/api-only` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [List Subaccount Domains](actions/list-subaccount-domains.md) | `GET /account/subaccount/:subaccount_id/domain` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [List Subaccount Orders](actions/list-subaccount-orders.md) | `GET /account/subaccount/:subaccount_id/order` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [List Subaccounts](actions/list-subaccounts.md) | `GET /account/subaccount` | [docs](https://dev.digicert.com/services-api/subaccount/list-subaccounts/) |
| [List Users](actions/list-users.md) | `GET /user` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhook` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
| [View Balance](actions/view-balance.md) | `GET /finance/balance` | [docs](https://dev.digicert.com/certcentral-apis/services-api.html) |
