# MoySklad: Native API Reference

A consolidated summary of MoySklad's API configuration and 156 documented operations, with links to official documentation.

- **Official docs:** https://dev.moysklad.ru/doc/api/remap/1.2/
- **API base URL:** `https://api.moysklad.ru/api/remap/1.2`

## Authentication

### API token

MoySklad API token sent as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dev.moysklad.ru/doc/api/remap/1.2/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json;charset=utf-8` |
| `Content-Type` | `application/json;charset=utf-8` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `contains`, `equals`, `greaterThan`, `greaterThanOrEquals`, `lessThan`, `lessThanOrEquals`.

## Sorting

Set the sort field with `order` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (156 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create counterparty](actions/create-counterparty.md) | `POST entity/counterparty` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-kontragent) |
| [Create customer order](actions/create-customer-order.md) | `POST entity/customerorder` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-zakaz-pokupatelia) |
| [Create document position](actions/create-document-position.md) | `POST entity/:entityType/:id/positions` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-obschie-swedeniia) |
| [Create document publication](actions/create-document-publication.md) | `POST entity/:entityType/:id/publication` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-publikaciia-dokumentow) |
| [Create entity attribute](actions/create-entity-attribute.md) | `POST entity/:entityType/metadata/attributes` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/workbook/#workbook-rabota-s-dopolnitelnymi-poliami-cherez-json-api) |
| [Create organization](actions/create-organization.md) | `POST entity/organization` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-iurlico) |
| [Create product](actions/create-product.md) | `POST entity/product` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-towar-sozdat-towar) |
| [Create service](actions/create-service.md) | `POST entity/service` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-usluga) |
| [Create store](actions/create-store.md) | `POST entity/store` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-sklad) |
| [Delete counterparty](actions/delete-counterparty.md) | `DELETE entity/counterparty/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-kontragent) |
| [Delete customer order](actions/delete-customer-order.md) | `DELETE entity/customerorder/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-zakaz-pokupatelia) |
| [Delete document position](actions/delete-document-position.md) | `DELETE entity/:entityType/:id/positions/:positionId` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-obschie-swedeniia) |
| [Delete entity attribute](actions/delete-entity-attribute.md) | `DELETE entity/:entityType/metadata/attributes/:attributeId` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/workbook/#workbook-rabota-s-dopolnitelnymi-poliami-cherez-json-api) |
| [Delete organization](actions/delete-organization.md) | `DELETE entity/organization/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-iurlico) |
| [Delete product](actions/delete-product.md) | `DELETE entity/product/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-towar) |
| [Delete service](actions/delete-service.md) | `DELETE entity/service/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-usluga) |
| [Delete store](actions/delete-store.md) | `DELETE entity/store/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-sklad) |
| [Get audit event](actions/get-audit-event.md) | `GET audit/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/audit/#audit-audit) |
| [Get bundle](actions/get-bundle.md) | `GET entity/bundle/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-komplekt-poluchit-komplekt) |
| [Get company settings](actions/get-company-settings.md) | `GET context/companysettings` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-nastroiki-kompanii) |
| [Get counterparty](actions/get-counterparty.md) | `GET entity/counterparty/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-kontragent-poluchit-kontragenta) |
| [Get counterparty report](actions/get-counterparty-report.md) | `GET report/counterparty` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-pokazateli-kontragentow) |
| [Get counterparty report by ID](actions/get-counterparty-report-by-id.md) | `GET report/counterparty/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-pokazateli-kontragentow) |
| [Get currency](actions/get-currency.md) | `GET entity/currency/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-valuta-poluchit-valutu) |
| [Get current stock by store report](actions/get-current-stock-by-store-report.md) | `GET report/stock/bystore/current` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-ostatki) |
| [Get current stock report](actions/get-current-stock-report.md) | `GET report/stock/all/current` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-ostatki) |
| [Get customer order](actions/get-customer-order.md) | `GET entity/customerorder/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-zakaz-pokupatelia) |
| [Get dashboard day](actions/get-dashboard-day.md) | `GET report/dashboard/day` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-pokazateli) |
| [Get dashboard month](actions/get-dashboard-month.md) | `GET report/dashboard/month` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-pokazateli) |
| [Get dashboard week](actions/get-dashboard-week.md) | `GET report/dashboard/week` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-pokazateli) |
| [Get document publication](actions/get-document-publication.md) | `GET entity/:entityType/:id/publication` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-publikaciia-dokumentow) |
| [Get employee](actions/get-employee.md) | `GET entity/employee/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-sotrudnik-poluchit-sotrudnika) |
| [Get entity metadata](actions/get-entity-metadata.md) | `GET entity/:entityType/metadata` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/workbook/#workbook-metadannye) |
| [Get group](actions/get-group.md) | `GET entity/group/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-otdel-poluchit-otdel) |
| [Get money by account report](actions/get-money-by-account-report.md) | `GET report/money/byaccount` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-dengi) |
| [Get money plot series report](actions/get-money-plot-series-report.md) | `GET report/money/plotseries` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-dengi) |
| [Get notification](actions/get-notification.md) | `GET notification/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/notification/#uwedomleniia-uwedomlenie) |
| [Get notification settings](actions/get-notification-settings.md) | `GET notification/settings` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/notification/#uwedomleniia-nastroiki-uwedomlenii) |
| [Get operations in transit report](actions/get-operations-in-transit-report.md) | `GET report/byoperations/intransit` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-po-dokumentam-nomenklatury) |
| [Get operations reserve report](actions/get-operations-reserve-report.md) | `GET report/byoperations/reserve` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-po-dokumentam-nomenklatury) |
| [Get operations stock report](actions/get-operations-stock-report.md) | `GET report/byoperations/stock` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-po-dokumentam-nomenklatury) |
| [Get orders plot series report](actions/get-orders-plot-series-report.md) | `GET report/orders/plotseries` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-pokazateli-prodazh-i-zakazow) |
| [Get organization](actions/get-organization.md) | `GET entity/organization/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-yurlico-poluchit-yurlico) |
| [Get product](actions/get-product.md) | `GET entity/product/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-towar-poluchit-towar) |
| [Get product folder](actions/get-product-folder.md) | `GET entity/productfolder/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-gruppa-towarow-poluchit-gruppu-towarow) |
| [Get profit by counterparty report](actions/get-profit-by-counterparty-report.md) | `GET report/profit/bycounterparty` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-pribylnost) |
| [Get profit by employee report](actions/get-profit-by-employee-report.md) | `GET report/profit/byemployee` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-pribylnost) |
| [Get profit by product report](actions/get-profit-by-product-report.md) | `GET report/profit/byproduct` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-pribylnost) |
| [Get profit by sales channel report](actions/get-profit-by-sales-channel-report.md) | `GET report/profit/bysaleschannel` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-pribylnost) |
| [Get profit by variant report](actions/get-profit-by-variant-report.md) | `GET report/profit/byvariant` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-pribylnost) |
| [Get sales plot series report](actions/get-sales-plot-series-report.md) | `GET report/sales/plotseries` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-pokazateli-prodazh-i-zakazow) |
| [Get service](actions/get-service.md) | `GET entity/service/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-usluga-poluchit-uslugu) |
| [Get stock by store report](actions/get-stock-by-store-report.md) | `GET report/stock/bystore` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-ostatki) |
| [Get stock report](actions/get-stock-report.md) | `GET report/stock/all` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-ostatki) |
| [Get store](actions/get-store.md) | `GET entity/store/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-sklad-poluchit-sklad) |
| [Get turnover by operations report](actions/get-turnover-by-operations-report.md) | `GET report/turnover/byoperations` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-oboroty) |
| [Get turnover by store report](actions/get-turnover-by-store-report.md) | `GET report/turnover/bystore` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-oboroty) |
| [Get turnover report](actions/get-turnover-report.md) | `GET report/turnover/all` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-oboroty) |
| [Get user settings](actions/get-user-settings.md) | `GET context/usersettings` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-nastroiki-polzowatelia) |
| [Get variant](actions/get-variant.md) | `GET entity/variant/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-modifikaciq-poluchit-modifikaciu) |
| [List assortment](actions/list-assortment.md) | `GET entity/assortment` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-assortiment) |
| [List audit event details](actions/list-audit-event-details.md) | `GET audit/:id/events` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/audit/#audit-audit) |
| [List audit events](actions/list-audit-events.md) | `GET audit` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/audit/#audit-audit) |
| [List audit filters metadata](actions/list-audit-filters-metadata.md) | `GET audit/metadata/filters` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/audit/#audit-audit) |
| [List bonus programs](actions/list-bonus-programs.md) | `GET entity/bonusprogram` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-bonusnaia-programma) |
| [List bundles](actions/list-bundles.md) | `GET entity/bundle` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-komplekt-poluchit-komplekty) |
| [List cash ins](actions/list-cash-ins.md) | `GET entity/cashin` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-prihodnyi-order) |
| [List cash outs](actions/list-cash-outs.md) | `GET entity/cashout` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-rashodnyi-order) |
| [List commission reports in](actions/list-commission-reports-in.md) | `GET entity/commissionreportin` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-poluchennyi-otchet-komissionera) |
| [List commission reports out](actions/list-commission-reports-out.md) | `GET entity/commissionreportout` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-wydannyi-otchet-komissionera) |
| [List consignments](actions/list-consignments.md) | `GET entity/consignment` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-partiia) |
| [List content cards](actions/list-content-cards.md) | `GET entity/contentcard` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-kartochka-kontenta) |
| [List contracts](actions/list-contracts.md) | `GET entity/contract` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-dogowor) |
| [List counterparties](actions/list-counterparties.md) | `GET entity/counterparty` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-kontragent-poluchit-kontragentow) |
| [List counterparty adjustments](actions/list-counterparty-adjustments.md) | `GET entity/counterpartyadjustment` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-korrektirowka-wzaimoraschetow) |
| [List countries](actions/list-countries.md) | `GET entity/country` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-strana-poluchit-strany) |
| [List currencies](actions/list-currencies.md) | `GET entity/currency` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-valuta-poluchit-valuty) |
| [List custom roles](actions/list-custom-roles.md) | `GET entity/role` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-polzowatelskie-roli) |
| [List custom templates](actions/list-custom-templates.md) | `GET entity/:entityType/metadata/customtemplate` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-shablon-pechatnoi-formy) |
| [List customer orders](actions/list-customer-orders.md) | `GET entity/customerorder` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#documents-zakaz-pokupatelq-poluchit-zakazy-pokupatelej) |
| [List demands](actions/list-demands.md) | `GET entity/demand` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#documents-otgruzka-poluchit-otgruzki) |
| [List discounts](actions/list-discounts.md) | `GET entity/discount` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-skidki) |
| [List document positions](actions/list-document-positions.md) | `GET entity/:entityType/:id/positions` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-obschie-swedeniia) |
| [List embedded templates](actions/list-embedded-templates.md) | `GET entity/:entityType/metadata/embeddedtemplate` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-shablon-pechatnoi-formy) |
| [List emission orders](actions/list-emission-orders.md) | `GET entity/emissionorder` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-zakaz-kodow-markirowki) |
| [List employees](actions/list-employees.md) | `GET entity/employee` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-sotrudnik-poluchit-sotrudnikow) |
| [List enters](actions/list-enters.md) | `GET entity/enter` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-oprihodowanie) |
| [List entity attributes](actions/list-entity-attributes.md) | `GET entity/:entityType/metadata/attributes` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/workbook/#workbook-rabota-s-dopolnitelnymi-poliami-cherez-json-api) |
| [List entity files](actions/list-entity-files.md) | `GET entity/:entityType/:id/files` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/workbook/#workbook-rabota-s-failami-v-dokumentah-nomenklature-i-kontragentah) |
| [List entity images](actions/list-entity-images.md) | `GET entity/:entityType/:id/images` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/workbook/#workbook-rabota-s-izobrazheniiami-v-towarah-modifikaciiakh-i-komplektah) |
| [List expense items](actions/list-expense-items.md) | `GET entity/expenseitem` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-statqia-rashodow) |
| [List facture ins](actions/list-facture-ins.md) | `GET entity/facturein` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-schet-faktura-poluchennyi) |
| [List facture outs](actions/list-facture-outs.md) | `GET entity/factureout` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-schet-faktura-wydannyi) |
| [List groups](actions/list-groups.md) | `GET entity/group` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-otdel-poluchit-otdely) |
| [List internal orders](actions/list-internal-orders.md) | `GET entity/internalorder` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-wnutrennii-zakaz) |
| [List inventories](actions/list-inventories.md) | `GET entity/inventory` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#documents-inventarizaciq-poluchit-inventarizacii) |
| [List invoices in](actions/list-invoices-in.md) | `GET entity/invoicein` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#documents-schet-postawschika-poluchit-scheta-postawschikow) |
| [List invoices out](actions/list-invoices-out.md) | `GET entity/invoiceout` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#documents-schet-pokupatelu-poluchit-scheta-pokupatelqm) |
| [List losses](actions/list-losses.md) | `GET entity/loss` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-spisanie) |
| [List moves](actions/list-moves.md) | `GET entity/move` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#documents-peremeschenie-poluchit-peremescheniq) |
| [List notifications](actions/list-notifications.md) | `GET notification` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/notification/#uwedomleniia-lenta-uwedomlenii) |
| [List organizations](actions/list-organizations.md) | `GET entity/organization` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-yurlico-poluchit-yurlica) |
| [List payments in](actions/list-payments-in.md) | `GET entity/paymentin` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#documents-vhodqschij-platezh-poluchit-vhodqschie-platezhi) |
| [List payments out](actions/list-payments-out.md) | `GET entity/paymentout` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#documents-ishodqschij-platezh-poluchit-ishodqschie-platezhi) |
| [List prepayment returns](actions/list-prepayment-returns.md) | `GET entity/prepaymentreturn` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-wozwrat-predoplaty) |
| [List prepayments](actions/list-prepayments.md) | `GET entity/prepayment` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-predoplata) |
| [List price lists](actions/list-price-lists.md) | `GET entity/pricelist` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-prais-list) |
| [List price types](actions/list-price-types.md) | `GET context/companysettings/pricetype` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-tipy-cen) |
| [List processing orders](actions/list-processing-orders.md) | `GET entity/processingorder` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-zakaz-na-proizwodstwo) |
| [List processing plan folders](actions/list-processing-plan-folders.md) | `GET entity/processingplanfolder` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-gruppa-tehkart) |
| [List processing plans](actions/list-processing-plans.md) | `GET entity/processingplan` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-tehkarta) |
| [List processing processes](actions/list-processing-processes.md) | `GET entity/processingprocess` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-tehprocess) |
| [List processing stages](actions/list-processing-stages.md) | `GET entity/processingstage` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-jetap-proizwodstwa) |
| [List processings](actions/list-processings.md) | `GET entity/processing` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-tehoperaciia) |
| [List product folders](actions/list-product-folders.md) | `GET entity/productfolder` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-gruppa-towarow-poluchit-gruppy-towarow) |
| [List product named filters](actions/list-product-named-filters.md) | `GET entity/product/namedfilter` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-sohranennye-filtry) |
| [List production stage completions](actions/list-production-stage-completions.md) | `GET entity/productionstagecompletion` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-wypolnenie-jetapa-proizwodstwa) |
| [List production tasks](actions/list-production-tasks.md) | `GET entity/productiontask` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-proizwodstwennoe-zadanie) |
| [List products](actions/list-products.md) | `GET entity/product` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-towar-poluchit-towary) |
| [List projects](actions/list-projects.md) | `GET entity/project` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-proekt) |
| [List purchase orders](actions/list-purchase-orders.md) | `GET entity/purchaseorder` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#documents-zakaz-postawschiku-poluchit-zakazy-postawschikam) |
| [List purchase returns](actions/list-purchase-returns.md) | `GET entity/purchasereturn` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-wozwrat-postawschiku) |
| [List regions](actions/list-regions.md) | `GET entity/region` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-region-poluchit-regiony) |
| [List retail demands](actions/list-retail-demands.md) | `GET entity/retaildemand` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-roznichnaia-prodazha) |
| [List retail drawer cash ins](actions/list-retail-drawer-cash-ins.md) | `GET entity/retaildrawercashin` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-wnesenie-deneg) |
| [List retail drawer cash outs](actions/list-retail-drawer-cash-outs.md) | `GET entity/retaildrawercashout` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-wyplata-deneg) |
| [List retail sales returns](actions/list-retail-sales-returns.md) | `GET entity/retailsalesreturn` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-roznichnyi-wozwrat) |
| [List retail shifts](actions/list-retail-shifts.md) | `GET entity/retailshift` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-roznichnaia-smena) |
| [List cashier retail store cashiers](actions/list-retail-store-cashiers.md) | `GET entity/retailstore/:retailStoreId/cashiers` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-kassir) |
| [List retail stores](actions/list-retail-stores.md) | `GET entity/retailstore` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-tochka-prodazh) |
| [List retire orders](actions/list-retire-orders.md) | `GET entity/retireorder` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-wywod-kodow-markirowki-iz-oborota) |
| [List sale platforms](actions/list-sale-platforms.md) | `GET entity/saleplatform` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-ploschadka-dlia-prodazh) |
| [List sales channels](actions/list-sales-channels.md) | `GET entity/saleschannel` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-kanal-prodazh) |
| [List sales returns](actions/list-sales-returns.md) | `GET entity/salesreturn` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-wozwrat-pokupatelia) |
| [List serial numbers](actions/list-serial-numbers.md) | `GET entity/thing` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-seriinyi-nomer) |
| [List services](actions/list-services.md) | `GET entity/service` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-usluga-poluchit-uslugi) |
| [List stock webhooks](actions/list-stock-webhooks.md) | `GET entity/webhookstock` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-vebhuk-na-izmenenie-ostatkow) |
| [List stores](actions/list-stores.md) | `GET entity/store` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-sklad-poluchit-sklady) |
| [List supplies](actions/list-supplies.md) | `GET entity/supply` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#documents-priemka-poluchit-priemki) |
| [List tasks](actions/list-tasks.md) | `GET entity/task` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-zadacha) |
| [List tax rates](actions/list-tax-rates.md) | `GET entity/taxrate` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-stawka-nds) |
| [List UOMs](actions/list-uoms.md) | `GET entity/uom` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-edinica-izmereniia) |
| [List variant characteristics](actions/list-variant-characteristics.md) | `GET entity/variant/metadata/characteristics` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-harakteristiki-modifikacii) |
| [List variants](actions/list-variants.md) | `GET entity/variant` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-modifikaciq-poluchit-modifikacii) |
| [List webhooks](actions/list-webhooks.md) | `GET entity/webhook` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-vebhuki) |
| [Mark all notifications as read](actions/mark-all-notifications-as-read.md) | `PUT notification/markasreadall` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/notification/#uwedomleniia-uwedomlenie) |
| [Mark notification as read](actions/mark-notification-as-read.md) | `PUT notification/:id/markasread` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/notification/#uwedomleniia-uwedomlenie) |
| [Update counterparty](actions/update-counterparty.md) | `PUT entity/counterparty/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-kontragent) |
| [Update customer order](actions/update-customer-order.md) | `PUT entity/customerorder/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-zakaz-pokupatelia) |
| [Update document position](actions/update-document-position.md) | `PUT entity/:entityType/:id/positions/:positionId` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-obschie-swedeniia) |
| [Update entity attribute](actions/update-entity-attribute.md) | `PUT entity/:entityType/metadata/attributes/:attributeId` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/workbook/#workbook-rabota-s-dopolnitelnymi-poliami-cherez-json-api) |
| [Update notification settings](actions/update-notification-settings.md) | `PUT notification/settings` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/notification/#uwedomleniia-nastroiki-uwedomlenii) |
| [Update organization](actions/update-organization.md) | `PUT entity/organization/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-iurlico) |
| [Update product](actions/update-product.md) | `PUT entity/product/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-towar) |
| [Update service](actions/update-service.md) | `PUT entity/service/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-usluga) |
| [Update store](actions/update-store.md) | `PUT entity/store/:id` | [docs](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-sklad) |
