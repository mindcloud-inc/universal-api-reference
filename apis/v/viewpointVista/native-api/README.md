# Viewpoint Vista: Native API Reference

A consolidated summary of Viewpoint Vista's API configuration and 65 documented operations, with links to official documentation.

- **Official docs:** https://direct-api.xchange.trimble.com/reference/setup
- **REST base URL:** `https://api.xchange.trimble.com/connect/`
- **Action Instance REST base URL:** `https://api.xchange.trimble.com/connect/`

## Authentication

### Custom

### Credentials

- **API Key:** `apiKey` · optional
- **Subscriber Code:** `subscriberCode` · optional

Send these headers with each API request:

```http
X-Application-Key: <apiKey>
```

## API conventions

### REST

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

The next-page cursor is read from `continuationToken`.

### Action Instance REST

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

- **REST:** Use `continuationToken` in the request body as the pagination cursor; numbering starts at 0.

## Filtering

- **REST:** Send filters in the request body.

## Endpoints (65 documented)

| Operation | API | Method & path | Vendor docs |
| --- | --- | --- | --- |
| [Add AR Contract Invoice V1](actions/add-ar-contract-invoice-v1.md) | REST | `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/ar/2/data/batch_entries/actions/add_contract_inv` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2databatch_entriesactionsadd_contract_inv_v2) |
| [Add Many Time Batch Entries](actions/add-many-payroll-timecard-entries.md) | REST | `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/pr/2/data/time_batch_entries/actions/add_many` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistapr2datatime_batch_entriesactionsadd_many) |
| [Add Non-Contract Invoice](actions/add-non-contract-invoice.md) | REST | `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/ar/2/data/batch_entries/actions/add_noncntrct_inv_v2` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistapr2datatime_batchesactionsupsert) |
| [Add Receipt Batch](actions/add-receipt-batch.md) | REST | `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/ar/2/data/batches/actions/add_receipt` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2databatchesactionsadd_receipt) |
| [Add Receipt Batch Entry](actions/add-receipt-batch-entry.md) | REST | `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/ar/2/data/batch_entries/actions/add_receipt` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2databatch_entriesactionsadd_receipt) |
| [Add SM Customer](actions/add-sm-customer.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/customers/actions/add` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2datacustomersactionsadd) |
| [Add SM Work Order](actions/add-sm-work-order.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/actions/add` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistasm2datawork_ordersactionsadd) |
| [Change SM Customer](actions/change-sm-customer.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/customers/actions/change` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistasm2datacustomersactionschange) |
| [Change SM Work Order](actions/change-sm-work-order.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/actions/change` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistasm2datawork_ordersactionschange) |
| [Create Contract](actions/create-contract.md) | REST | `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/jc/2/data/contracts/actions/add` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistajc2datajobsactionsadd) |
| [Create Customer Action](actions/create-customer-action.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/customers/actions/add` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2datacustomersactionsadd) |
| [Create JC Job](actions/create-jc-job.md) | REST | `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/jc/2/data/jobs/actions/add` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistajc2datajobsactionsadd) |
| [Get Action Instance](actions/get-action-instance.md) | Action Instance REST | `GET v1/direct/actions/:action_key_value` | [docs](https://direct-api.xchange.trimble.com/reference/get-directactionsaction_key_value) |
| [Get Customer by RyvitId](actions/get-customer-by-ryvit-id.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/sm/2/data/customers/cache/__ryvitId/:ryvitId_value` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache__ryvitidryvitid_value) |
| [Get Customer by SMCo, CustGroup, Customer](actions/get-customer-by-sm-co-cust-group-customer.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/sm/2/data/customers/cache/natural/:SMCo/:CustGroup/:Customer` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistasm2datacustomerscachesearchsearch) |
| [Get Customer by SMCustomerID](actions/get-customer-by-sm-customer-id.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/sm/2/data/customers/cache/id/:SMCustomerID` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistasm2datacustomerscachesearchsearch) |
| [Get Service Site by SMServiceSiteID](actions/get-service-site-by-sm-service-site-id.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/sm/2/data/service_sites/cache/id/:SMServiceSiteID` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistasm2datacustomerscachesearchsearch) |
| [Get Timecard Batch by Ryvit ID](actions/get-timecard-batch-by-ryvit-id.md) | REST | `GET v1/direct/subscribers/{{credentials.subscriberCode}}/vista/pr/2/data/time_batches/cache/:ryvitId_value` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistapr2datatime_batchescacheryvitid_value) |
| [List AP Objects](actions/list-ap-objects.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [List AR Objects](actions/list-ar-objects.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [List DM Objects](actions/list-dm-objects.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [List EM Objects](actions/list-em-objects.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [List GL Objects](actions/list-gl-objects.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [List HQ Objects](actions/list-hq-objects.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [List HR Objects](actions/list-hr-objects.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [List IN Objects](actions/list-in-objects.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [List JC Objects](actions/list-jc-objects.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [List MS Objects](actions/list-ms-objects.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [List PM Objects](actions/list-pm-objects.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [List PO Objects](actions/list-po-objects.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [List Potential Projects](actions/list-potential-projects.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [List PR Objects](actions/list-pr-objects.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [List SL Objects](actions/list-sl-objects.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [List SM Objects](actions/list-sm-objects.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [List UD Objects](actions/list-ud-objects.md) | REST | `GET v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [Post Invoice Batch](actions/post-invoice-batch.md) | REST | `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/ar/2/data/batches/actions/post_invoice` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistapr2datatime_batchesactionsupsert) |
| [Post Payment Batch](actions/post-payment-batch.md) | REST | `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/ar/2/data/batches/actions/post_receipt` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistapr2datatime_batchesactionsupsert) |
| [Search AP Objects](actions/search-ap-objects.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [Search AR Objects](actions/search-ar-objects.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [Search Batch Entries](actions/search-batch-entries.md) | REST | `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/ar/2/data/batch_entries/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2datatransactionscachesearchsearch) |
| [Search Batches](actions/search-batches.md) | REST | `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/ar/2/data/batches/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2databatchescachesearchsearch) |
| [Search DM Objects](actions/search-dm-objects.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [Search EM Objects](actions/search-em-objects.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [Search GL Objects](actions/search-gl-objects.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [Search HQ Objects](actions/search-hq-objects.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [Search HR Objects](actions/search-hr-objects.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [Search IN Objects](actions/search-in-objects.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [Search JC Objects](actions/search-jc-objects.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [Search MS Objects](actions/search-ms-objects.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [Search PM Objects](actions/search-pm-objects.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [Search PO Objects](actions/search-po-objects.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [Search Potential Projects](actions/search-potential-projects.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [Search PR Objects](actions/search-pr-objects.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [Search SL Objects](actions/search-sl-objects.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [Search SM Objects](actions/search-sm-objects.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [Search Transactions](actions/search-transactions.md) | REST | `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/ar/2/data/transactions/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2datatransactionscachesearchsearch) |
| [Search UD Objects](actions/search-ud-objects.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` | [docs](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache) |
| [Update Contract](actions/update-contract.md) | REST | `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/jc/2/data/contracts/actions/change` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistajc2datajobsactionsadd) |
| [Update Customer Action](actions/update-customer-action.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/customers/actions/change` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2datacustomersactionsadd) |
| [Update JC Job](actions/update-jc-job.md) | REST | `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/jc/2/data/jobs/actions/change` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistajc2datajobsactionsadd) |
| [Update Vendor](actions/update-vendor.md) | REST | `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/vendors/actions/change` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaap2datavendorsactionschange) |
| [Upsert AR Invoice Batch](actions/upsert-ar-invoice-batch.md) | REST | `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/ar/2/data/batches/actions/add_invoice` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2databatchesactionsadd_invoice) |
| [Upsert Invoice Batch](actions/upsert-invoice-batch.md) | REST | `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/ar/2/data/batches/actions/upsert_invoice` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistapr2datatime_batchesactionsupsert) |
| [Upsert Receipt Batch](actions/upsert-receipt-batch.md) | REST | `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/ar/2/data/batches/actions/upsert_receipt` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2databatchesactionsupsert_receipt) |
| [Upsert Timecard Batch](actions/upsert-timecard-batch.md) | REST | `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/pr/2/data/time_batches/actions/upsert` | [docs](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistapr2datatime_batchesactionsupsert) |
