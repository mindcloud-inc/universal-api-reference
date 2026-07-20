# <img src="https://images.mindcloud.co/apps/icons/digi-cert_1775824975599.png" alt="DigiCert logo" width="28" height="28"> DigiCert: Universal API

DigiCert lets you manage CertCentral accounts, domains, organizations, certificate orders, users, products, webhooks, finance, and related Services API resources from one integration.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/digiCert/latest
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.digicert.com/
- **Vendor API docs:** https://dev.digicert.com/certcentral-apis/services-api.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Details](actions/get-account-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiCert/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves your CertCentral account details from DigiCert. |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Get API Key Details](actions/get-api-key-details.md) | GET | Retrieves details for an API key in DigiCert. |
| [List API Keys](actions/list-api-keys.md) | GET | Retrieves API keys from your DigiCert account. |

### Auth Key

| Action | Method | Description |
| --- | --- | --- |
| [Get Auth Key Details](actions/get-auth-key-details.md) | GET | Retrieves details for an AuthKey in DigiCert. |
| [List Auth Keys](actions/list-auth-keys.md) | GET | Retrieves active AuthKeys linked to your DigiCert account. |

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [View Balance](actions/view-balance.md) | GET | Retrieves your current DigiCert account balance. |

### Container

| Action | Method | Description |
| --- | --- | --- |
| [Get Container Details](actions/get-container-details.md) | GET | Retrieves details for a container in DigiCert. |
| [List Containers](actions/list-containers.md) | GET | Retrieves containers from your DigiCert account. |

### Contract

| Action | Method | Description |
| --- | --- | --- |
| [Get Contract Details](actions/get-contract-details.md) | GET | Retrieves active contract details from your DigiCert account. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Details](actions/get-domain-details.md) | GET | Retrieves details for a domain in DigiCert. |
| [List Domains](actions/list-domains.md) | GET | Retrieves domains from your DigiCert account. |

### Domain Dcv Method

| Action | Method | Description |
| --- | --- | --- |
| [List Domain DCV Methods](actions/list-domain-dcv-methods.md) | GET | Retrieves available domain DCV methods from DigiCert. |

### Domain Validation

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Validation Details](actions/get-domain-validation-details.md) | GET | Retrieves validation details for a domain in DigiCert. |

### Domain Validation Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Validation Types](actions/get-domain-validation-types.md) | GET | Retrieves available domain validation types from DigiCert. |

### Duplicate

| Action | Method | Description |
| --- | --- | --- |
| [List Duplicates](actions/list-duplicates.md) | GET | Retrieves duplicate certificates for a DigiCert order. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Details](actions/get-order-details.md) | GET | Retrieves details for a certificate order in DigiCert. |
| [List Orders](actions/list-orders.md) | GET | Retrieves certificate orders from your DigiCert account. |

### Order Note

| Action | Method | Description |
| --- | --- | --- |
| [List Order Notes](actions/list-order-notes.md) | GET | Retrieves notes for a DigiCert certificate order. |

### Order Validation

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Validation Status](actions/get-order-validation-status.md) | GET | Retrieves validation status for a DigiCert order. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Details](actions/get-organization-details.md) | GET | Retrieves details for an organization in DigiCert. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from your DigiCert account. |

### Organization Approver

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Approvers](actions/list-organization-approvers.md) | GET | Retrieves potential organization approvers from DigiCert. |

### Organization Validation

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Validation Details](actions/get-organization-validation-details.md) | GET | Retrieves validation details for an organization in DigiCert. |

### Permission

| Action | Method | Description |
| --- | --- | --- |
| [Check Permission](actions/check-permission.md) | GET | Checks whether the authenticated user has a DigiCert permission. |
| [List Permissions](actions/list-permissions.md) | GET | Retrieves permissions for the authenticated DigiCert user. |

### Pricing

| Action | Method | Description |
| --- | --- | --- |
| [List Pricing](actions/list-pricing.md) | GET | Retrieves product pricing from your DigiCert account. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Details](actions/get-product-details.md) | GET | Retrieves details for a DigiCert product. |
| [List Products](actions/list-products.md) | GET | Retrieves products available to your DigiCert account. |

### Reissue

| Action | Method | Description |
| --- | --- | --- |
| [List Reissues](actions/list-reissues.md) | GET | Retrieves certificate reissues for a DigiCert order. |

### Service User

| Action | Method | Description |
| --- | --- | --- |
| [List Service Users](actions/list-service-users.md) | GET | Retrieves service users from your DigiCert account. |

### Subaccount

| Action | Method | Description |
| --- | --- | --- |
| [Get Subaccount Details](actions/get-subaccount-details.md) | GET | Retrieves details for a DigiCert subaccount. |
| [List Subaccounts](actions/list-subaccounts.md) | GET | Retrieves subaccounts from your DigiCert account. |

### Subaccount Domain

| Action | Method | Description |
| --- | --- | --- |
| [List Subaccount Domains](actions/list-subaccount-domains.md) | GET | Retrieves domain details from a DigiCert subaccount. |

### Subaccount Order

| Action | Method | Description |
| --- | --- | --- |
| [List Subaccount Orders](actions/list-subaccount-orders.md) | GET | Retrieves orders from a DigiCert subaccount and its children. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Details](actions/get-user-details.md) | GET | Retrieves details for a user in DigiCert. |
| [List Users](actions/list-users.md) | GET | Retrieves users from your DigiCert account. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from your DigiCert account. |

### Webhook Event Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook Event Logs](actions/get-webhook-event-logs.md) | GET | Retrieves event logs for a DigiCert webhook. |

