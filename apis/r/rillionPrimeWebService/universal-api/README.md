# <img src="https://images.mindcloud.co/apps/icons/rillion-prime-web-service_1785258584935.png" alt="Rillion Prime Web Service logo" width="28" height="28"> Rillion Prime Web Service: Universal API

Exchange invoices, purchase orders, and master data with Rillion Prime AP automation through its SOAP web service.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rillionPrimeWebService/latest
- **Category:** Commerce / Accounting
- **Actions:** 56
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.rillion.com
- **Vendor API docs:** https://support.rillion.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Count Account Coded Invoices](actions/count-account-coded-invoices.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/count-account-coded-invoices?connectionId=$CONNECTION_ID&invoiceSeries=string&invoiceNo=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (56)

### Accounting Periods

| Action | Method | Description |
| --- | --- | --- |
| [Insert Period](actions/insert-period.md) | POST | Insert an accounting period into the Prime register queue. |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Insert Asset](actions/insert-asset.md) | POST | Insert an asset into the Prime register queue. |
| [Insert Asset Type](actions/insert-asset-type.md) | POST | Insert an asset type into the Prime register queue. |

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [Insert Event Log](actions/insert-event-log.md) | POST | Write an event log entry in Rillion Prime. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Commodity](actions/get-commodity.md) | GET | Get one commodity by identifier. |
| [Insert Commodity](actions/insert-commodity.md) | POST | Insert a commodity into the Prime register queue. |
| [List Commodities](actions/list-commodities.md) | GET | List commodities in Rillion Prime. |

### Code Relation

| Action | Method | Description |
| --- | --- | --- |
| [Insert Code Relation](actions/insert-code-relation.md) | POST | Insert a coding relation into the Prime register queue. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Insert Company](actions/insert-company.md) | POST | Insert a company into the Prime register queue. |
| [List Companies](actions/list-companies.md) | GET | List the company identifiers available in the connected Rillion Prime environment. |
| [List Company Data](actions/list-company-data.md) | GET | List configuration data for one company in Rillion Prime. |

### Custom Setting

| Action | Method | Description |
| --- | --- | --- |
| [Insert Custom Setting](actions/insert-custom-setting.md) | POST | Insert a custom setting in Rillion Prime. Administrative operation — changes Prime configuration. Undocumented details: confirm with… |
| [List Custom Settings](actions/list-custom-settings.md) | GET | List custom settings in Rillion Prime. Administrative operation. |
| [Update Custom Setting](actions/update-custom-setting.md) | PUT | Update a custom setting in Rillion Prime. Administrative operation — changes Prime configuration. Undocumented details: confirm with… |

### Dimensions

| Action | Method | Description |
| --- | --- | --- |
| [Insert Object](actions/insert-object.md) | POST | Insert an accounting object (coding dimension value) into the Prime register queue. |
| [Insert Object Type](actions/insert-object-type.md) | POST | Insert an accounting object type (coding dimension) into the Prime register queue. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Send Email](actions/send-email.md) | POST | Send an email through Rillion Prime. Side-effectful — Prime delivers the email to its recipients. |

### Environments

| Action | Method | Description |
| --- | --- | --- |
| [List Environment Data](actions/list-environment-data.md) | GET | List configuration data for the connected Rillion Prime environment. |
| [List Environments](actions/list-environments.md) | GET | List the Rillion Prime environment names available to the connected login. |

### Erp

| Action | Method | Description |
| --- | --- | --- |
| [List ERPs](actions/list-erps.md) | GET | List the ERP systems configured in Rillion Prime. |

### Exchange Rates

| Action | Method | Description |
| --- | --- | --- |
| [Insert Currency](actions/insert-currency.md) | POST | Insert a currency exchange rate into the Prime register queue. |

### Goods Receipts

| Action | Method | Description |
| --- | --- | --- |
| [Insert Purchase Order Delivery](actions/insert-purchase-order-delivery.md) | POST | Register a delivery against a purchase order in Prime. |
| [Insert Purchase Order Receipt](actions/insert-purchase-order-receipt.md) | POST | Insert a purchase order receipt in Prime. |

### Holiday

| Action | Method | Description |
| --- | --- | --- |
| [Insert Holiday](actions/insert-holiday.md) | POST | Insert a holiday calendar entry into the Prime register queue. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Count Account Coded Invoices](actions/count-account-coded-invoices.md) | GET | Count how many times an invoice has been account coded. |
| [Get Invoice Image](actions/get-invoice-image.md) | GET | Get the stored image files for one invoice. |
| [Insert Invoice](actions/insert-invoice.md) | POST | Insert an invoice into the Prime invoice queue. |
| [Insert Invoice Receipt by UQ](actions/insert-invoice-receipt-by-uq.md) | POST | Insert an invoice receipt identified by its unique key (company, supplier, supplier invoice number). |
| [List Invoices](actions/list-invoices.md) | GET | List invoices from the Prime invoice queue. |
| [List Invoices ERP](actions/list-invoices-erp.md) | GET | List invoices from the Prime invoice queue for one ERP. |
| [List Invoices for Update in ERP](actions/list-invoices-for-update-in-erp.md) | GET | List invoices with updated account coding that should be updated in the ERP. |
| [List Invoices Missing Payment Date](actions/list-invoices-missing-payment-date.md) | GET | List invoices that have no payment date registered in Prime. |
| [List Invoices Ready for Deletion](actions/list-invoices-ready-for-deletion.md) | GET | List invoices marked ready for deletion in the Prime invoice queue. |
| [List Invoices Ready for Deletion ERP](actions/list-invoices-ready-for-deletion-erp.md) | GET | List invoices marked ready for deletion for one ERP. |
| [List Invoices Ready for Final Recording](actions/list-invoices-ready-for-final-recording.md) | GET | List approved invoices ready for definite recording in the ERP. |
| [List Invoices Ready for Final Recording ERP](actions/list-invoices-ready-for-final-recording-erp.md) | GET | List approved invoices ready for definite recording for one ERP. |
| [List Invoices Ready for Preliminary Recording](actions/list-invoices-ready-for-preliminary-recording.md) | GET | List invoices ready for preliminary recording in the ERP. |
| [List Invoices Ready for Preliminary Recording ERP](actions/list-invoices-ready-for-preliminary-recording-erp.md) | GET | List invoices ready for preliminary recording for one ERP. |
| [Send Invoice Reply](actions/send-invoice-reply.md) | PUT | Confirm back to Prime how an exported invoice was processed in the ERP. |
| [Set Invoice Payment Date](actions/set-invoice-payment-date.md) | PUT | Register the payment date for an invoice in Prime. |
| [Set Invoice Payment Date by UQ](actions/set-invoice-payment-date-by-uq.md) | PUT | Register the payment date for an invoice identified by its unique key. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Insert Item](actions/insert-item.md) | POST | Insert a purchasing item into the Prime register queue. |
| [List Items](actions/list-items.md) | GET | List purchasing items in Rillion Prime. |

### Ledger Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Insert Account](actions/insert-account.md) | POST | Insert a general ledger account into the Prime register queue. |

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [Delete Purchase Order](actions/delete-purchase-order.md) | DELETE | Delete a purchase order from Prime. Undocumented in the vendor guide — confirm semantics with Rillion before production use. |
| [Insert Purchase Order](actions/insert-purchase-order.md) | POST | Insert a purchase order into the Prime purchase order queue. |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | List purchase orders from the Prime purchase order queue by status. |
| [List Purchase Orders ERP](actions/list-purchase-orders-erp.md) | GET | List purchase orders from the Prime purchase order queue by status for one ERP. |
| [Synchronize Purchase Order](actions/synchronize-purchase-order.md) | PUT | Synchronize an existing purchase order in Prime with the ERP version. Undocumented in the vendor guide — confirm semantics with Rillion… |

### Queues

| Action | Method | Description |
| --- | --- | --- |
| [List Item Queues](actions/list-item-queues.md) | GET | List entries in the Prime item queue. |
| [Process Item Queue](actions/process-item-queue.md) | PUT | Trigger processing of the Prime item queue. Administrative operation — understand queue state before running. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [Insert User Profile Role](actions/insert-user-profile-role.md) | POST | Insert a user profile role assignment into the Prime register queue. Administrative operation. |

### System

| Action | Method | Description |
| --- | --- | --- |
| [Get Version](actions/get-version.md) | GET | Get the Rillion Prime web service version. |

### Tax Codes

| Action | Method | Description |
| --- | --- | --- |
| [Insert VAT Code](actions/insert-vat-code.md) | POST | Insert a VAT code into the Prime register queue. |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [Insert Supplier](actions/insert-supplier.md) | POST | Insert a supplier into the Prime register queue. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Insert Dynamic Flow](actions/insert-dynamic-flow.md) | POST | Insert a dynamic approval flow into the Prime register queue. |

