# <img src="https://images.mindcloud.co/apps/icons/image-56_1768253248612.png" alt="PestPac logo" width="28" height="28"> PestPac: Universal API

PestPac through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pestpac/latest
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://developer.workwave.com/documentation#pestpac

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [CompanySetup](actions/company-setup.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/company-setup?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get Access Token](actions/get-access-token.md) | POST |  |

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity Log](actions/get-activity-log.md) | GET |  |

### Bill To

| Action | Method | Description |
| --- | --- | --- |
| [Get Bill](actions/get-bill.md) | GET |  |

### Company Setup

| Action | Method | Description |
| --- | --- | --- |
| [CompanySetup](actions/company-setup.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [List Contacts by Location Id](actions/list-contacts-by-location-id.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [UserDefFields](actions/user-def-fields.md) | GET |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST |  |
| [Get Documents by Location ID](actions/get-documents-by-location-id.md) | GET |  |
| [Update Document](actions/update-document.md) | PUT |  |
| [Upload Document](actions/upload-document.md) | PUT |  |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [List Employees](actions/list-employees.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoices](actions/get-invoices.md) | GET |  |
| [Get Test](actions/get-test.md) | GET |  |
| [List Invoices by ID](actions/list-invoices-by-id.md) | GET |  |
| [List Unpaid Invoices by Location Id](actions/list-unpaid-invoices-by-location-id.md) | GET |  |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Leads](actions/leads.md) | GET |  |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST |  |
| [Get Locations](actions/get-locations.md) | GET |  |
| [List Location IDs](actions/list-location-i-ds.md) | GET |  |
| [Update Location](actions/update-location.md) | PUT |  |

### Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookups](actions/lookups.md) | GET |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment](actions/create-payment.md) | POST |  |
| [Get Payment History By BillToId](actions/get-payment-history-by-bill-to-id.md) | GET |  |
| [Get Payments](actions/get-payments.md) | GET |  |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [List Schedules](actions/list-schedules.md) | GET |  |

### Service Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Service Orders](actions/get-orders.md) | GET |  |
| [Get Service Order Attributes](actions/get-service-order-attributes.md) | GET |  |
| [Get Service Orders by id](actions/get-service-orders-by-id.md) | GET |  |
| [List Service Orders](actions/list-service-orders.md) | GET |  |
| [List Service Orders by Location ID](actions/list-service-orders-by-location-id.md) | GET |  |

### Service Setup

| Action | Method | Description |
| --- | --- | --- |
| [Get Service Setups](actions/get-service-setups.md) | GET |  |
| [List Service Setups by Location ID](actions/list-service-setups-by-location-id.md) | GET |  |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Get Services](actions/get-services.md) | GET |  |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Update Webhook](actions/update-webhook.md) | PUT |  |
| [Get Webhooks](actions/web-hooks.md) | GET |  |

