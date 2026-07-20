# <img src="https://images.mindcloud.co/apps/icons/moysklad-icon-square_1776778861417.png" alt="MoySklad logo" width="28" height="28"> MoySklad: Universal API

MoySklad is a cloud inventory, sales, purchasing, warehouse, and document management platform. This app connects to the MoySklad JSON API 1.2 for managing catalog entities, counterparties, documents, reports, audit events, notifications, and related business records.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/moySklad/latest
- **Category:** Commerce / ERP
- **Actions:** 156
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.moysklad.ru/
- **Vendor API docs:** https://dev.moysklad.ru/doc/api/remap/1.2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (156)

### Assortment

| Action | Method | Description |
| --- | --- | --- |
| [List assortment](actions/list-assortment.md) | GET | Retrieves assortment from MoySklad. |

### Audit Event

| Action | Method | Description |
| --- | --- | --- |
| [Get audit event](actions/get-audit-event.md) | GET | Retrieves the audit event from MoySklad. |
| [List audit events](actions/list-audit-events.md) | GET | Retrieves audit events from MoySklad. |

### Audit Event Detail

| Action | Method | Description |
| --- | --- | --- |
| [List audit event details](actions/list-audit-event-details.md) | GET | Retrieves audit event details from MoySklad. |

### Audit Filter Metadata

| Action | Method | Description |
| --- | --- | --- |
| [List audit filters metadata](actions/list-audit-filters-metadata.md) | GET | Retrieves audit filters metadata from MoySklad. |

### Bonus Program

| Action | Method | Description |
| --- | --- | --- |
| [List bonus programs](actions/list-bonus-programs.md) | GET | Retrieves bonus programs from MoySklad. |

### Bundle

| Action | Method | Description |
| --- | --- | --- |
| [Get bundle](actions/get-bundle.md) | GET | Retrieves the bundle from MoySklad. |
| [List bundles](actions/list-bundles.md) | GET | Retrieves bundles from MoySklad. |

### Cash In

| Action | Method | Description |
| --- | --- | --- |
| [List cash ins](actions/list-cash-ins.md) | GET | Retrieves cash ins from MoySklad. |

### Cash Out

| Action | Method | Description |
| --- | --- | --- |
| [List cash outs](actions/list-cash-outs.md) | GET | Retrieves cash outs from MoySklad. |

### Cashier

| Action | Method | Description |
| --- | --- | --- |
| [List cashier retail store cashiers](actions/list-retail-store-cashiers.md) | GET | Retrieves cashier retail store cashiers from MoySklad. |

### Commission Report In

| Action | Method | Description |
| --- | --- | --- |
| [List commission reports in](actions/list-commission-reports-in.md) | GET | Retrieves commission reports in from MoySklad. |

### Commission Report Out

| Action | Method | Description |
| --- | --- | --- |
| [List commission reports out](actions/list-commission-reports-out.md) | GET | Retrieves commission reports out from MoySklad. |

### Company Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get company settings](actions/get-company-settings.md) | GET | Retrieves the company settings from MoySklad. |

### Consignment

| Action | Method | Description |
| --- | --- | --- |
| [List consignments](actions/list-consignments.md) | GET | Retrieves consignments from MoySklad. |

### Content Card

| Action | Method | Description |
| --- | --- | --- |
| [List content cards](actions/list-content-cards.md) | GET | Retrieves content cards from MoySklad. |

### Contract

| Action | Method | Description |
| --- | --- | --- |
| [List contracts](actions/list-contracts.md) | GET | Retrieves contracts from MoySklad. |

### Counterparty

| Action | Method | Description |
| --- | --- | --- |
| [Create counterparty](actions/create-counterparty.md) | POST | Creates a counterparty in MoySklad. |
| [Delete counterparty](actions/delete-counterparty.md) | DELETE | Deletes a counterparty from MoySklad. |
| [Get counterparty](actions/get-counterparty.md) | GET | Retrieves the counterparty from MoySklad. |
| [List counterparties](actions/list-counterparties.md) | GET | Retrieves counterparties from MoySklad. |
| [Update counterparty](actions/update-counterparty.md) | PUT | Updates a counterparty in MoySklad. |

### Counterparty Adjustment

| Action | Method | Description |
| --- | --- | --- |
| [List counterparty adjustments](actions/list-counterparty-adjustments.md) | GET | Retrieves counterparty adjustments from MoySklad. |

### Counterparty Report

| Action | Method | Description |
| --- | --- | --- |
| [Get counterparty report](actions/get-counterparty-report.md) | GET | Retrieves the counterparty report from MoySklad. |
| [Get counterparty report by ID](actions/get-counterparty-report-by-id.md) | GET | Retrieves the counterparty report from MoySklad by ID. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List countries](actions/list-countries.md) | GET | Retrieves countries from MoySklad. |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [Get currency](actions/get-currency.md) | GET | Retrieves the currency from MoySklad. |
| [List currencies](actions/list-currencies.md) | GET | Retrieves currencies from MoySklad. |

### Current Stock By Store Report

| Action | Method | Description |
| --- | --- | --- |
| [Get current stock by store report](actions/get-current-stock-by-store-report.md) | GET | Retrieves the current stock by store report from MoySklad. |

### Current Stock Report

| Action | Method | Description |
| --- | --- | --- |
| [Get current stock report](actions/get-current-stock-report.md) | GET | Retrieves the current stock report from MoySklad. |

### Custom Role

| Action | Method | Description |
| --- | --- | --- |
| [List custom roles](actions/list-custom-roles.md) | GET | Retrieves custom roles from MoySklad. |

### Custom Template

| Action | Method | Description |
| --- | --- | --- |
| [List custom templates](actions/list-custom-templates.md) | GET | Retrieves custom templates from MoySklad. |

### Customer Order

| Action | Method | Description |
| --- | --- | --- |
| [Create customer order](actions/create-customer-order.md) | POST | Creates a customer order in MoySklad. |
| [Delete customer order](actions/delete-customer-order.md) | DELETE | Deletes a customer order from MoySklad. |
| [Get customer order](actions/get-customer-order.md) | GET | Retrieves the customer order from MoySklad. |
| [List customer orders](actions/list-customer-orders.md) | GET | Retrieves customer orders from MoySklad. |
| [Update customer order](actions/update-customer-order.md) | PUT | Updates a customer order in MoySklad. |

### Dashboard Day

| Action | Method | Description |
| --- | --- | --- |
| [Get dashboard day](actions/get-dashboard-day.md) | GET | Retrieves the dashboard day from MoySklad. |

### Dashboard Month

| Action | Method | Description |
| --- | --- | --- |
| [Get dashboard month](actions/get-dashboard-month.md) | GET | Retrieves the dashboard month from MoySklad. |

### Dashboard Week

| Action | Method | Description |
| --- | --- | --- |
| [Get dashboard week](actions/get-dashboard-week.md) | GET | Retrieves the dashboard week from MoySklad. |

### Demand

| Action | Method | Description |
| --- | --- | --- |
| [List demands](actions/list-demands.md) | GET | Retrieves demands from MoySklad. |

### Discount

| Action | Method | Description |
| --- | --- | --- |
| [List discounts](actions/list-discounts.md) | GET | Retrieves discounts from MoySklad. |

### Document Position

| Action | Method | Description |
| --- | --- | --- |
| [Create document position](actions/create-document-position.md) | POST | Creates a document position in MoySklad. |
| [Delete document position](actions/delete-document-position.md) | DELETE | Deletes a document position from MoySklad. |
| [List document positions](actions/list-document-positions.md) | GET | Retrieves document positions from MoySklad. |
| [Update document position](actions/update-document-position.md) | PUT | Updates a document position in MoySklad. |

### Document Publication

| Action | Method | Description |
| --- | --- | --- |
| [Create document publication](actions/create-document-publication.md) | POST | Creates a document publication in MoySklad. |
| [Get document publication](actions/get-document-publication.md) | GET | Retrieves the document publication from MoySklad. |

### Embedded Template

| Action | Method | Description |
| --- | --- | --- |
| [List embedded templates](actions/list-embedded-templates.md) | GET | Retrieves embedded templates from MoySklad. |

### Emission Order

| Action | Method | Description |
| --- | --- | --- |
| [List emission orders](actions/list-emission-orders.md) | GET | Retrieves emission orders from MoySklad. |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Get employee](actions/get-employee.md) | GET | Retrieves the employee from MoySklad. |
| [List employees](actions/list-employees.md) | GET | Retrieves employees from MoySklad. |

### Enter

| Action | Method | Description |
| --- | --- | --- |
| [List enters](actions/list-enters.md) | GET | Retrieves enters from MoySklad. |

### Entity Attribute

| Action | Method | Description |
| --- | --- | --- |
| [Create entity attribute](actions/create-entity-attribute.md) | POST | Creates an entity attribute in MoySklad. |
| [Delete entity attribute](actions/delete-entity-attribute.md) | DELETE | Deletes an entity attribute from MoySklad. |
| [List entity attributes](actions/list-entity-attributes.md) | GET | Retrieves entity attributes from MoySklad. |
| [Update entity attribute](actions/update-entity-attribute.md) | PUT | Updates an entity attribute in MoySklad. |

### Entity File

| Action | Method | Description |
| --- | --- | --- |
| [List entity files](actions/list-entity-files.md) | GET | Retrieves entity files from MoySklad. |

### Entity Image

| Action | Method | Description |
| --- | --- | --- |
| [List entity images](actions/list-entity-images.md) | GET | Retrieves entity images from MoySklad. |

### Entity Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get entity metadata](actions/get-entity-metadata.md) | GET | Retrieves the entity metadata from MoySklad. |

### Expense Item

| Action | Method | Description |
| --- | --- | --- |
| [List expense items](actions/list-expense-items.md) | GET | Retrieves expense items from MoySklad. |

### Facture In

| Action | Method | Description |
| --- | --- | --- |
| [List facture ins](actions/list-facture-ins.md) | GET | Retrieves facture ins from MoySklad. |

### Facture Out

| Action | Method | Description |
| --- | --- | --- |
| [List facture outs](actions/list-facture-outs.md) | GET | Retrieves facture outs from MoySklad. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get group](actions/get-group.md) | GET | Retrieves the group from MoySklad. |
| [List groups](actions/list-groups.md) | GET | Retrieves groups from MoySklad. |

### Internal Order

| Action | Method | Description |
| --- | --- | --- |
| [List internal orders](actions/list-internal-orders.md) | GET | Retrieves internal orders from MoySklad. |

### Inventory

| Action | Method | Description |
| --- | --- | --- |
| [List inventories](actions/list-inventories.md) | GET | Retrieves inventories from MoySklad. |

### Invoice In

| Action | Method | Description |
| --- | --- | --- |
| [List invoices in](actions/list-invoices-in.md) | GET | Retrieves invoices in from MoySklad. |

### Invoice Out

| Action | Method | Description |
| --- | --- | --- |
| [List invoices out](actions/list-invoices-out.md) | GET | Retrieves invoices out from MoySklad. |

### Loss

| Action | Method | Description |
| --- | --- | --- |
| [List losses](actions/list-losses.md) | GET | Retrieves losses from MoySklad. |

### Money By Account Report

| Action | Method | Description |
| --- | --- | --- |
| [Get money by account report](actions/get-money-by-account-report.md) | GET | Retrieves the money by account report from MoySklad. |

### Money Plot Series Report

| Action | Method | Description |
| --- | --- | --- |
| [Get money plot series report](actions/get-money-plot-series-report.md) | GET | Retrieves the money plot series report from MoySklad. |

### Move

| Action | Method | Description |
| --- | --- | --- |
| [List moves](actions/list-moves.md) | GET | Retrieves moves from MoySklad. |

### Named Filter

| Action | Method | Description |
| --- | --- | --- |
| [List product named filters](actions/list-product-named-filters.md) | GET | Retrieves product named filters from MoySklad. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Get notification](actions/get-notification.md) | GET | Retrieves the notification from MoySklad. |
| [List notifications](actions/list-notifications.md) | GET | Retrieves notifications from MoySklad. |
| [Mark all notifications as read](actions/mark-all-notifications-as-read.md) | PUT | Marks all notifications as read in MoySklad. |
| [Mark notification as read](actions/mark-notification-as-read.md) | PUT | Marks a notification as read in MoySklad. |

### Notification Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get notification settings](actions/get-notification-settings.md) | GET | Retrieves the notification settings from MoySklad. |
| [Update notification settings](actions/update-notification-settings.md) | PUT | Updates notification settings in MoySklad. |

### Operations In Transit Report

| Action | Method | Description |
| --- | --- | --- |
| [Get operations in transit report](actions/get-operations-in-transit-report.md) | GET | Retrieves the operations in transit report from MoySklad. |

### Operations Reserve Report

| Action | Method | Description |
| --- | --- | --- |
| [Get operations reserve report](actions/get-operations-reserve-report.md) | GET | Retrieves the operations reserve report from MoySklad. |

### Operations Stock Report

| Action | Method | Description |
| --- | --- | --- |
| [Get operations stock report](actions/get-operations-stock-report.md) | GET | Retrieves the operations stock report from MoySklad. |

### Orders Plot Series Report

| Action | Method | Description |
| --- | --- | --- |
| [Get orders plot series report](actions/get-orders-plot-series-report.md) | GET | Retrieves the orders plot series report from MoySklad. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Create organization](actions/create-organization.md) | POST | Creates an organization in MoySklad. |
| [Delete organization](actions/delete-organization.md) | DELETE | Deletes an organization from MoySklad. |
| [Get organization](actions/get-organization.md) | GET | Retrieves the organization from MoySklad. |
| [List organizations](actions/list-organizations.md) | GET | Retrieves organizations from MoySklad. |
| [Update organization](actions/update-organization.md) | PUT | Updates an organization in MoySklad. |

### Payment In

| Action | Method | Description |
| --- | --- | --- |
| [List payments in](actions/list-payments-in.md) | GET | Retrieves payments in from MoySklad. |

### Payment Out

| Action | Method | Description |
| --- | --- | --- |
| [List payments out](actions/list-payments-out.md) | GET | Retrieves payments out from MoySklad. |

### Prepayment

| Action | Method | Description |
| --- | --- | --- |
| [List prepayments](actions/list-prepayments.md) | GET | Retrieves prepayments from MoySklad. |

### Prepayment Return

| Action | Method | Description |
| --- | --- | --- |
| [List prepayment returns](actions/list-prepayment-returns.md) | GET | Retrieves prepayment returns from MoySklad. |

### Price List

| Action | Method | Description |
| --- | --- | --- |
| [List price lists](actions/list-price-lists.md) | GET | Retrieves price lists from MoySklad. |

### Price Type

| Action | Method | Description |
| --- | --- | --- |
| [List price types](actions/list-price-types.md) | GET | Retrieves price types from MoySklad. |

### Processing

| Action | Method | Description |
| --- | --- | --- |
| [List processings](actions/list-processings.md) | GET | Retrieves processings from MoySklad. |

### Processing Order

| Action | Method | Description |
| --- | --- | --- |
| [List processing orders](actions/list-processing-orders.md) | GET | Retrieves processing orders from MoySklad. |

### Processing Plan

| Action | Method | Description |
| --- | --- | --- |
| [List processing plans](actions/list-processing-plans.md) | GET | Retrieves processing plans from MoySklad. |

### Processing Plan Folder

| Action | Method | Description |
| --- | --- | --- |
| [List processing plan folders](actions/list-processing-plan-folders.md) | GET | Retrieves processing plan folders from MoySklad. |

### Processing Process

| Action | Method | Description |
| --- | --- | --- |
| [List processing processes](actions/list-processing-processes.md) | GET | Retrieves processing processes from MoySklad. |

### Processing Stage

| Action | Method | Description |
| --- | --- | --- |
| [List processing stages](actions/list-processing-stages.md) | GET | Retrieves processing stages from MoySklad. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create product](actions/create-product.md) | POST | Creates a product in MoySklad. |
| [Delete product](actions/delete-product.md) | DELETE | Deletes a product from MoySklad. |
| [Get product](actions/get-product.md) | GET | Retrieves the product from MoySklad. |
| [List products](actions/list-products.md) | GET | Retrieves products from MoySklad. |
| [Update product](actions/update-product.md) | PUT | Updates a product in MoySklad. |

### Product Folder

| Action | Method | Description |
| --- | --- | --- |
| [Get product folder](actions/get-product-folder.md) | GET | Retrieves the product folder from MoySklad. |
| [List product folders](actions/list-product-folders.md) | GET | Retrieves product folders from MoySklad. |

### Production Stage Completion

| Action | Method | Description |
| --- | --- | --- |
| [List production stage completions](actions/list-production-stage-completions.md) | GET | Retrieves production stage completions from MoySklad. |

### Production Task

| Action | Method | Description |
| --- | --- | --- |
| [List production tasks](actions/list-production-tasks.md) | GET | Retrieves production tasks from MoySklad. |

### Profit By Counterparty Report

| Action | Method | Description |
| --- | --- | --- |
| [Get profit by counterparty report](actions/get-profit-by-counterparty-report.md) | GET | Retrieves the profit by counterparty report from MoySklad. |

### Profit By Employee Report

| Action | Method | Description |
| --- | --- | --- |
| [Get profit by employee report](actions/get-profit-by-employee-report.md) | GET | Retrieves the profit by employee report from MoySklad. |

### Profit By Product Report

| Action | Method | Description |
| --- | --- | --- |
| [Get profit by product report](actions/get-profit-by-product-report.md) | GET | Retrieves the profit by product report from MoySklad. |

### Profit By Sales Channel Report

| Action | Method | Description |
| --- | --- | --- |
| [Get profit by sales channel report](actions/get-profit-by-sales-channel-report.md) | GET | Retrieves the profit by sales channel report from MoySklad. |

### Profit By Variant Report

| Action | Method | Description |
| --- | --- | --- |
| [Get profit by variant report](actions/get-profit-by-variant-report.md) | GET | Retrieves the profit by variant report from MoySklad. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List projects](actions/list-projects.md) | GET | Retrieves projects from MoySklad. |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [List purchase orders](actions/list-purchase-orders.md) | GET | Retrieves purchase orders from MoySklad. |

### Purchase Return

| Action | Method | Description |
| --- | --- | --- |
| [List purchase returns](actions/list-purchase-returns.md) | GET | Retrieves purchase returns from MoySklad. |

### Region

| Action | Method | Description |
| --- | --- | --- |
| [List regions](actions/list-regions.md) | GET | Retrieves regions from MoySklad. |

### Retail Demand

| Action | Method | Description |
| --- | --- | --- |
| [List retail demands](actions/list-retail-demands.md) | GET | Retrieves retail demands from MoySklad. |

### Retail Drawer Cash In

| Action | Method | Description |
| --- | --- | --- |
| [List retail drawer cash ins](actions/list-retail-drawer-cash-ins.md) | GET | Retrieves retail drawer cash ins from MoySklad. |

### Retail Drawer Cash Out

| Action | Method | Description |
| --- | --- | --- |
| [List retail drawer cash outs](actions/list-retail-drawer-cash-outs.md) | GET | Retrieves retail drawer cash outs from MoySklad. |

### Retail Sales Return

| Action | Method | Description |
| --- | --- | --- |
| [List retail sales returns](actions/list-retail-sales-returns.md) | GET | Retrieves retail sales returns from MoySklad. |

### Retail Shift

| Action | Method | Description |
| --- | --- | --- |
| [List retail shifts](actions/list-retail-shifts.md) | GET | Retrieves retail shifts from MoySklad. |

### Retail Store

| Action | Method | Description |
| --- | --- | --- |
| [List retail stores](actions/list-retail-stores.md) | GET | Retrieves retail stores from MoySklad. |

### Retire Order

| Action | Method | Description |
| --- | --- | --- |
| [List retire orders](actions/list-retire-orders.md) | GET | Retrieves retire orders from MoySklad. |

### Sale Platform

| Action | Method | Description |
| --- | --- | --- |
| [List sale platforms](actions/list-sale-platforms.md) | GET | Retrieves sale platforms from MoySklad. |

### Sales Channel

| Action | Method | Description |
| --- | --- | --- |
| [List sales channels](actions/list-sales-channels.md) | GET | Retrieves sales channels from MoySklad. |

### Sales Plot Series Report

| Action | Method | Description |
| --- | --- | --- |
| [Get sales plot series report](actions/get-sales-plot-series-report.md) | GET | Retrieves the sales plot series report from MoySklad. |

### Sales Return

| Action | Method | Description |
| --- | --- | --- |
| [List sales returns](actions/list-sales-returns.md) | GET | Retrieves sales returns from MoySklad. |

### Serial Number

| Action | Method | Description |
| --- | --- | --- |
| [List serial numbers](actions/list-serial-numbers.md) | GET | Retrieves serial numbers from MoySklad. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Create service](actions/create-service.md) | POST | Creates a service in MoySklad. |
| [Delete service](actions/delete-service.md) | DELETE | Deletes a service from MoySklad. |
| [Get service](actions/get-service.md) | GET | Retrieves the service from MoySklad. |
| [List services](actions/list-services.md) | GET | Retrieves services from MoySklad. |
| [Update service](actions/update-service.md) | PUT | Updates a service in MoySklad. |

### Stock By Store Report

| Action | Method | Description |
| --- | --- | --- |
| [Get stock by store report](actions/get-stock-by-store-report.md) | GET | Retrieves the stock by store report from MoySklad. |

### Stock Report

| Action | Method | Description |
| --- | --- | --- |
| [Get stock report](actions/get-stock-report.md) | GET | Retrieves the stock report from MoySklad. |

### Stock Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List stock webhooks](actions/list-stock-webhooks.md) | GET | Retrieves stock webhooks from MoySklad. |

### Store

| Action | Method | Description |
| --- | --- | --- |
| [Create store](actions/create-store.md) | POST | Creates a store in MoySklad. |
| [Delete store](actions/delete-store.md) | DELETE | Deletes a store from MoySklad. |
| [Get store](actions/get-store.md) | GET | Retrieves the store from MoySklad. |
| [List stores](actions/list-stores.md) | GET | Retrieves stores from MoySklad. |
| [Update store](actions/update-store.md) | PUT | Updates a store in MoySklad. |

### Supply

| Action | Method | Description |
| --- | --- | --- |
| [List supplies](actions/list-supplies.md) | GET | Retrieves supplies from MoySklad. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [List tasks](actions/list-tasks.md) | GET | Retrieves tasks from MoySklad. |

### Tax Rate

| Action | Method | Description |
| --- | --- | --- |
| [List tax rates](actions/list-tax-rates.md) | GET | Retrieves tax rates from MoySklad. |

### Turnover By Operations Report

| Action | Method | Description |
| --- | --- | --- |
| [Get turnover by operations report](actions/get-turnover-by-operations-report.md) | GET | Retrieves the turnover by operations report from MoySklad. |

### Turnover By Store Report

| Action | Method | Description |
| --- | --- | --- |
| [Get turnover by store report](actions/get-turnover-by-store-report.md) | GET | Retrieves the turnover by store report from MoySklad. |

### Turnover Report

| Action | Method | Description |
| --- | --- | --- |
| [Get turnover report](actions/get-turnover-report.md) | GET | Retrieves the turnover report from MoySklad. |

### Uom

| Action | Method | Description |
| --- | --- | --- |
| [List UOMs](actions/list-uoms.md) | GET | Retrieves UOMs from MoySklad. |

### User Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get user settings](actions/get-user-settings.md) | GET | Retrieves the user settings from MoySklad. |

### Variant

| Action | Method | Description |
| --- | --- | --- |
| [Get variant](actions/get-variant.md) | GET | Retrieves the variant from MoySklad. |
| [List variants](actions/list-variants.md) | GET | Retrieves variants from MoySklad. |

### Variant Characteristic

| Action | Method | Description |
| --- | --- | --- |
| [List variant characteristics](actions/list-variant-characteristics.md) | GET | Retrieves variant characteristics from MoySklad. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from MoySklad. |

