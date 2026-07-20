# Ascora: Native API Reference

A consolidated summary of Ascora's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://support.ascora.com.au/display/AS/API+Endpoints
- **API base URL:** `https://api.ascora.com.au`

## Authentication

### API Key

Use an Ascora Auth key generated in Administration > API Settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Auth: <apiKey>
```

[Official authentication documentation](https://support.ascora.com.au/display/AS/Ascora+Enquiry+API)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `PageSize` in the query string to set the page size (default 250). Use `Page` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Kits To Quote](actions/add-kits-to-quote.md) | `POST /Quotes/AddKits` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=33) |
| [Add Labour To Quote](actions/add-labour-to-quote.md) | `POST /Quotes/AddLabourItems` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=36) |
| [Add Quote Sections](actions/add-quote-sections.md) | `POST /Quotes/AddQuoteSections` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=40) |
| [Add Supplies To Quote](actions/add-supplies-to-quote.md) | `POST /Quotes/AddSupplies` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=32) |
| [Add Write-Ins To Quote](actions/add-write-ins-to-quote.md) | `POST /Quotes/AddWriteIns` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=34) |
| [Clear Quote Items](actions/clear-quote-items.md) | `POST /Quotes/ClearQuoteItems` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=39) |
| [Create Customer](actions/create-customer.md) | `POST /Customers/Customer` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=13) |
| [Create Enquiry](actions/create-enquiry.md) | `POST /Enquiry` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=4) |
| [Create Full Section-Based Quote](actions/create-full-section-based-quote.md) | `POST /Quotes/Quote` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=41) |
| [Create Job](actions/create-job.md) | `POST /Jobs/Job` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=53) |
| [Create Payment](actions/create-payment.md) | `POST /Accounting/CreatePayment` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=77) |
| [Create Quote](actions/create-quote.md) | `POST /Quotes/Quote` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=27) |
| [Create Quote With Items](actions/create-quote-with-items.md) | `POST /Quotes/Quote` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=37) |
| [Create Supplier](actions/create-supplier.md) | `POST /Suppliers/Supplier` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=67) |
| [Create Supplier Invoice](actions/create-supplier-invoice.md) | `POST /SupplierInvoices/SupplierInvoice` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=57) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /WebHooks` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=69) |
| [Delete Quote Or Section](actions/delete-quote-or-section.md) | `POST /Quotes/DeleteQuote` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=45) |
| [Get Customer](actions/get-customer.md) | `GET /Customers/Customer/{{id}}` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=9) |
| [Get Invoices To Send](actions/get-invoices-to-send.md) | `GET /Accounting/GetInvoicesToSend` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=71) |
| [Get Job](actions/get-job.md) | `GET /Jobs/Job/{{jobNumber}}` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=49) |
| [Get Payments To Send](actions/get-payments-to-send.md) | `GET /Accounting/GetPaymentsToSend` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=76) |
| [Get Quote](actions/get-quote.md) | `GET /Quotes/Quote/{{quoteNumber}}` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=23) |
| [Get Supplier Invoice](actions/get-supplier-invoice.md) | `GET /SupplierInvoices/SupplierInvoice/{{id}}` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=62) |
| [List Categories](actions/list-categories.md) | `GET /Inventory/Categories` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=19) |
| [List Contacts](actions/list-contacts.md) | `GET /Customers/Contacts` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=10) |
| [List Contacts For Customer](actions/list-contacts-for-customer.md) | `GET /Customers/GetContactsForCustomer/{{customerId}}` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=11) |
| [List Customers](actions/list-customers.md) | `GET /Customers/Customers` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=7) |
| [List Jobs](actions/list-jobs.md) | `GET /Jobs/Jobs` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=52) |
| [List Kits](actions/list-kits.md) | `GET /Inventory/Kits` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=18) |
| [List Labour Roles](actions/list-labour-roles.md) | `GET /Quotes/LabourRoles` | [docs](https://support.ascora.com.au/display/AS/API+Endpoints) |
| [List Quotes](actions/list-quotes.md) | `GET /Quotes/Quotes` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=25) |
| [List Supplier Invoices](actions/list-supplier-invoices.md) | `GET /SupplierInvoices/SupplierInvoices` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=59) |
| [List Suppliers](actions/list-suppliers.md) | `GET /Suppliers/Suppliers` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=64) |
| [List Supplies](actions/list-supplies.md) | `GET /Inventory/Supplies` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=16) |
| [Mark Invoices Sent](actions/mark-invoices-sent.md) | `POST /Accounting/MarkInvoicesAsSent` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=75) |
| [Mark Payments Sent](actions/mark-payments-sent.md) | `POST /Accounting/MarkPaymentsAsSent` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=79) |
| [Update Customer](actions/update-customer.md) | `POST /Customers/Customer` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=13) |
| [Update Quote Status](actions/update-quote-status.md) | `POST /Quotes/UpdateStatus` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=44) |
| [Update Supplier](actions/update-supplier.md) | `POST /Suppliers/Supplier` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=67) |
| [Upsert Contact](actions/upsert-contact.md) | `POST /Customers/Contact` | [docs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=12) |
