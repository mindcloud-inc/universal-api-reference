# <img src="https://images.mindcloud.co/apps/icons/billingo_1776739451691.png" alt="Billingo logo" width="28" height="28"> Billingo: Universal API

Billingo is a Hungarian online invoicing and business administration platform. This integration connects to the Billingo API v3 for invoices, partners, products, spending records, bank accounts, organization data, utilities, and related read workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/billingo/latest
- **Category:** Commerce / Accounting
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.billingo.hu/
- **Vendor API docs:** https://developers.billingo.hu/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Server Time](actions/get-server-time.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-server-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Bank Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Bank Account](actions/get-bank-account.md) | GET | Retrieves a bank account from Billingo. |
| [List Bank Accounts](actions/list-bank-accounts.md) | GET | Retrieves bank account records from Billingo. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Document](actions/get-document.md) | GET | Retrieves a document record from Billingo. |
| [Get Document By Vendor ID](actions/get-document-by-vendor-id.md) | GET | Retrieves a document from Billingo by vendor ID. |
| [List Documents](actions/list-documents.md) | GET | Retrieves document records from your Billingo account. |

### Document Block

| Action | Method | Description |
| --- | --- | --- |
| [List Document Blocks](actions/list-document-blocks.md) | GET | Retrieves document blocks from your Billingo account. |

### Document Export

| Action | Method | Description |
| --- | --- | --- |
| [Poll Document Export](actions/poll-document-export.md) | GET | Retrieves a document export status from Billingo. |

### Document Export File

| Action | Method | Description |
| --- | --- | --- |
| [Download Document Export](actions/download-document-export.md) | GET | Retrieves an exported document file from Billingo. |

### Document Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Download Document](actions/download-document.md) | GET | Retrieves a document PDF from Billingo. |

### Document Public Url

| Action | Method | Description |
| --- | --- | --- |
| [Get Document Public URL](actions/get-document-public-url.md) | GET | Retrieves a public document download URL from Billingo. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Copy Document](actions/copy-document.md) | POST | Creates a copy of a document in Billingo. |
| [Create Document From Proforma](actions/create-document-from-proforma.md) | POST | Creates a document from a proforma in Billingo. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Send Document](actions/send-document.md) | POST | Sends a document to email recipients in Billingo. |

### Exchange Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get Currency Conversion Rate](actions/get-currency-conversion-rate.md) | GET | Retrieves currency conversion rates from Billingo. |

### Export Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Create Document Export](actions/create-document-export.md) | POST | Creates a new document export in Billingo. |

### Inventory Levels

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Inventory Quantity](actions/get-product-inventory-quantity.md) | GET | Retrieves product quantity from Billingo's default warehouse. |

### Legacy Id Conversion

| Action | Method | Description |
| --- | --- | --- |
| [Convert Legacy ID](actions/convert-legacy-id.md) | GET | Retrieves a Billingo v3 ID from legacy ID. |

### Online Szamla Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Document Online Szamla Status](actions/get-document-online-szamla-status.md) | GET | Retrieves a document Online Szamla status from Billingo. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves organization details from your Billingo account. |

### Partner

| Action | Method | Description |
| --- | --- | --- |
| [Get Partner](actions/get-partner.md) | GET |  |
| [List Partners](actions/list-partners.md) | GET | Retrieves partner records from your Billingo account. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Get Document Payments](actions/get-document-payments.md) | GET | Retrieves payment history for a document in Billingo. |

### Pos Print Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Print POS Document](actions/print-pos-document.md) | GET | Retrieves a printable POS document from Billingo. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product record from Billingo. |
| [List Products](actions/list-products.md) | GET | Retrieves product records from your Billingo account. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [List Document Reminders](actions/list-document-reminders.md) | GET | Retrieves document reminders from Billingo by status. |

### Server Time

| Action | Method | Description |
| --- | --- | --- |
| [Get Server Time](actions/get-server-time.md) | GET | Retrieves the current server time from Billingo. |

### Spending

| Action | Method | Description |
| --- | --- | --- |
| [Get Spending](actions/get-spending.md) | GET | Retrieves a spending record from Billingo. |
| [List Spendings](actions/list-spendings.md) | GET | Retrieves spending items from Billingo by due date. |

### Tax Number Check

| Action | Method | Description |
| --- | --- | --- |
| [Check Tax Number](actions/check-tax-number.md) | GET | Retrieves tax number validation details from Billingo. |

