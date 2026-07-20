# <img src="https://images.mindcloud.co/apps/icons/vtiger-crm_1774008556650.png" alt="Vtiger CRM logo" width="28" height="28"> Vtiger CRM: Universal API

Connect Vtiger CRM to read and manage CRM records, module metadata, and tenant data through the Vtiger REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vtigerCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.vtiger.com/
- **Vendor API docs:** https://vtap.vtiger.com/platform/rest-apis.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST | Creates a new account in Vtiger CRM. |
| [List Accounts](actions/list-accounts.md) | GET | Finds accounts in Vtiger CRM by query. |

### Account Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Describe Accounts](actions/describe-accounts.md) | GET | Retrieves account metadata from Vtiger CRM. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Vtiger CRM. |
| [List Contacts](actions/list-contacts.md) | GET | Finds contacts in Vtiger CRM by query. |

### Contact Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Describe Contacts](actions/describe-contacts.md) | GET | Retrieves contact metadata from Vtiger CRM. |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in Vtiger CRM. |
| [List Deals](actions/list-deals.md) | GET | Finds deals in Vtiger CRM by query. |

### Deal Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Describe Deals](actions/describe-deals.md) | GET | Retrieves deal metadata from Vtiger CRM. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Vtiger CRM. |
| [List Invoices](actions/list-invoices.md) | GET | Finds invoices in Vtiger CRM by query. |

### Invoice Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Describe Invoices](actions/describe-invoices.md) | GET | Retrieves invoice metadata from Vtiger CRM. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in Vtiger CRM. |
| [List Leads](actions/list-leads.md) | GET | Finds leads in Vtiger CRM by query. |

### Lead Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Describe Leads](actions/describe-leads.md) | GET | Retrieves lead metadata from Vtiger CRM. |

### Module

| Action | Method | Description |
| --- | --- | --- |
| [List Modules](actions/list-modules.md) | GET | Retrieves accessible modules from Vtiger CRM. |

### Module Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Describe Module](actions/describe-module.md) | GET | Retrieves module metadata from Vtiger CRM. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Vtiger CRM. |
| [List Products](actions/list-products.md) | GET | Finds products in Vtiger CRM by query. |

### Product Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Describe Products](actions/describe-products.md) | GET | Retrieves product metadata from Vtiger CRM. |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase Order](actions/create-purchase-order.md) | POST | Creates a new purchase order in Vtiger CRM. |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Finds purchase orders in Vtiger CRM by query. |

### Purchase Order Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Describe Purchase Orders](actions/describe-purchase-orders.md) | GET | Retrieves purchase order metadata from Vtiger CRM. |

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [Create Quote](actions/create-quote.md) | POST | Creates a new quote in Vtiger CRM. |
| [List Quotes](actions/list-quotes.md) | GET | Finds quotes in Vtiger CRM by query. |

### Quote Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Describe Quotes](actions/describe-quotes.md) | GET | Retrieves quote metadata from Vtiger CRM. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | POST | Creates a new record in Vtiger CRM. |
| [Delete Record](actions/delete-record.md) | DELETE | Deletes an existing record from Vtiger CRM. |
| [Query Records](actions/query-records.md) | GET | Finds records in Vtiger CRM by query string. |
| [Retrieve Record](actions/retrieve-record.md) | GET | Retrieves a record from Vtiger CRM. |
| [Revise Record](actions/revise-record.md) | PUT | Updates an existing record in Vtiger CRM. |

### Sales Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Sales Order](actions/create-sales-order.md) | POST | Creates a new sales order in Vtiger CRM. |
| [List Sales Orders](actions/list-sales-orders.md) | GET | Finds sales orders in Vtiger CRM by query. |

### Sales Order Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Describe Sales Orders](actions/describe-sales-orders.md) | GET | Retrieves sales order metadata from Vtiger CRM. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user profile from Vtiger CRM. |

### Vendor

| Action | Method | Description |
| --- | --- | --- |
| [Create Vendor](actions/create-vendor.md) | POST | Creates a new vendor in Vtiger CRM. |
| [List Vendors](actions/list-vendors.md) | GET | Finds vendors in Vtiger CRM by query. |

### Vendor Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Describe Vendors](actions/describe-vendors.md) | GET | Retrieves vendor metadata from Vtiger CRM. |

