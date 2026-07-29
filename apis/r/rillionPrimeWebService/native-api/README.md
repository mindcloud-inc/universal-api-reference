# Rillion Prime Web Service: Native API Reference

A consolidated summary of Rillion Prime Web Service's API configuration and 56 documented operations, with links to official documentation.

- **Official docs:** https://support.rillion.com
- **API base URL:** `{baseUrl}`

## Authentication

### Custom

### Credentials

- **Web Service URL:** `baseUrl` · required · The full URL of your Rillion Prime web service endpoint.
- **Environment:** `environment` · required · The Rillion Prime environment (instance) name your credentials belong to. Your Rillion contact can confirm it.
- **Login Name:** `loginName` · required
- **Password:** `password` · required

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/soap+xml; charset=utf-8` |

## Endpoints (56 documented)

| Operation | Method & path |
| --- | --- |
| [Count Account Coded Invoices](actions/count-account-coded-invoices.md) | `POST` |
| [Delete Purchase Order](actions/delete-purchase-order.md) | `POST` |
| [Get Commodity](actions/get-commodity.md) | `POST` |
| [Get Invoice Image](actions/get-invoice-image.md) | `POST` |
| [Get Version](actions/get-version.md) | `POST` |
| [Insert Account](actions/insert-account.md) | `POST` |
| [Insert Asset](actions/insert-asset.md) | `POST` |
| [Insert Asset Type](actions/insert-asset-type.md) | `POST` |
| [Insert Code Relation](actions/insert-code-relation.md) | `POST` |
| [Insert Commodity](actions/insert-commodity.md) | `POST` |
| [Insert Company](actions/insert-company.md) | `POST` |
| [Insert Currency](actions/insert-currency.md) | `POST` |
| [Insert Custom Setting](actions/insert-custom-setting.md) | `POST` |
| [Insert Dynamic Flow](actions/insert-dynamic-flow.md) | `POST` |
| [Insert Event Log](actions/insert-event-log.md) | `POST` |
| [Insert Holiday](actions/insert-holiday.md) | `POST` |
| [Insert Invoice](actions/insert-invoice.md) | `POST` |
| [Insert Invoice Receipt by UQ](actions/insert-invoice-receipt-by-uq.md) | `POST` |
| [Insert Item](actions/insert-item.md) | `POST` |
| [Insert Object](actions/insert-object.md) | `POST` |
| [Insert Object Type](actions/insert-object-type.md) | `POST` |
| [Insert Period](actions/insert-period.md) | `POST` |
| [Insert Purchase Order](actions/insert-purchase-order.md) | `POST` |
| [Insert Purchase Order Delivery](actions/insert-purchase-order-delivery.md) | `POST` |
| [Insert Purchase Order Receipt](actions/insert-purchase-order-receipt.md) | `POST` |
| [Insert Supplier](actions/insert-supplier.md) | `POST` |
| [Insert User Profile Role](actions/insert-user-profile-role.md) | `POST` |
| [Insert VAT Code](actions/insert-vat-code.md) | `POST` |
| [List Commodities](actions/list-commodities.md) | `POST` |
| [List Companies](actions/list-companies.md) | `POST` |
| [List Company Data](actions/list-company-data.md) | `POST` |
| [List Custom Settings](actions/list-custom-settings.md) | `POST` |
| [List Environment Data](actions/list-environment-data.md) | `POST` |
| [List Environments](actions/list-environments.md) | `POST` |
| [List ERPs](actions/list-erps.md) | `POST` |
| [List Invoices](actions/list-invoices.md) | `POST` |
| [List Invoices ERP](actions/list-invoices-erp.md) | `POST` |
| [List Invoices for Update in ERP](actions/list-invoices-for-update-in-erp.md) | `POST` |
| [List Invoices Missing Payment Date](actions/list-invoices-missing-payment-date.md) | `POST` |
| [List Invoices Ready for Deletion](actions/list-invoices-ready-for-deletion.md) | `POST` |
| [List Invoices Ready for Deletion ERP](actions/list-invoices-ready-for-deletion-erp.md) | `POST` |
| [List Invoices Ready for Final Recording](actions/list-invoices-ready-for-final-recording.md) | `POST` |
| [List Invoices Ready for Final Recording ERP](actions/list-invoices-ready-for-final-recording-erp.md) | `POST` |
| [List Invoices Ready for Preliminary Recording](actions/list-invoices-ready-for-preliminary-recording.md) | `POST` |
| [List Invoices Ready for Preliminary Recording ERP](actions/list-invoices-ready-for-preliminary-recording-erp.md) | `POST` |
| [List Item Queues](actions/list-item-queues.md) | `POST` |
| [List Items](actions/list-items.md) | `POST` |
| [List Purchase Orders](actions/list-purchase-orders.md) | `POST` |
| [List Purchase Orders ERP](actions/list-purchase-orders-erp.md) | `POST` |
| [Process Item Queue](actions/process-item-queue.md) | `POST` |
| [Send Email](actions/send-email.md) | `POST` |
| [Send Invoice Reply](actions/send-invoice-reply.md) | `POST` |
| [Set Invoice Payment Date](actions/set-invoice-payment-date.md) | `POST` |
| [Set Invoice Payment Date by UQ](actions/set-invoice-payment-date-by-uq.md) | `POST` |
| [Synchronize Purchase Order](actions/synchronize-purchase-order.md) | `POST` |
| [Update Custom Setting](actions/update-custom-setting.md) | `POST` |
