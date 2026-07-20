# Print.one Postcards: Native API Reference

A consolidated summary of Print.one Postcards's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://api.print.one/docs/v2
- **OpenAPI specification:** https://api.print.one/docs/v2/swagger.json
- **API base URL:** `https://api.print.one`

## Authentication

### API Key

Connect with a Print.one TEST or LIVE API key from the portal.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://help.print.one/api/authentication-and-api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `pages`. The current page number is read from `page`.

## Pagination

Use `limit` in the query string to set the page size (default 20; maximum 200). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sortBy` in the query string. Use `ASC` for ascending order and `DESC` for descending order. Multiple sort fields can be combined.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Orders To Batch](actions/add-orders-to-batch.md) | `POST /v2/batches/:batchId/orders` | [docs](https://api.print.one/docs/v2#operation/Batch/addBatchOrder) |
| [Archive Batch](actions/archive-batch.md) | `POST /v2/batches/:batchId/archive` | [docs](https://api.print.one/docs/v2#operation/Batch/archiveBatch) |
| [Cancel Batch](actions/cancel-batch.md) | `POST /v2/batches/:batchId/cancel` | [docs](https://api.print.one/docs/v2#operation/Batch/cancelBatch) |
| [Cancel Batch CSV Import](actions/cancel-batch-csv-import.md) | `POST /v2/batches/:batchId/csv/:csvId/cancel` | [docs](https://api.print.one/docs/v2#operation/Batch/cancelCsvImport) |
| [Cancel Batch Order](actions/cancel-batch-order.md) | `POST /v2/batches/:batchId/orders/:orderId/cancel` | [docs](https://api.print.one/docs/v2#operation/Batch/cancelOrder) |
| [Cancel Order](actions/cancel-order.md) | `POST /v2/orders/:id/cancel` | [docs](https://api.print.one/docs/v2#operation/Order/cancelOrder) |
| [Create Batch](actions/create-batch.md) | `POST /v2/batches` | [docs](https://api.print.one/docs/v2#operation/Batch/createBatch) |
| [Create Order](actions/create-order.md) | `POST /v2/orders` | [docs](https://api.print.one/docs/v2#operation/Order/createOrder) |
| [Create Template](actions/create-template.md) | `POST /v2/templates` | [docs](https://api.print.one/docs/v2#operation/Template/createTemplate) |
| [Create Template Preview](actions/create-template-preview.md) | `POST /v2/templates/preview/[:id]/[:version]` | [docs](https://api.print.one/docs/v2#operation/Template/createTemplatePreview) |
| [Delete Custom File](actions/delete-custom-file.md) | `DELETE /v2/customfiles/[:fileId]` | [docs](https://api.print.one/docs/v2#operation/CustomFiles/deleteCustomFile) |
| [Delete Template](actions/delete-template.md) | `DELETE /v2/templates/[:id]` | [docs](https://api.print.one/docs/v2#operation/Template/deleteTemplate) |
| [Download Custom File](actions/download-custom-file.md) | `GET /v2/customfiles/[:fileId]/download` | [docs](https://api.print.one/docs/v2#operation/CustomFiles/downloadCustomFile) |
| [Duplicate Template](actions/duplicate-template.md) | `POST /v2/templates/duplicate/[:id]` | [docs](https://api.print.one/docs/v2#operation/Template/duplicateTemplate) |
| [Get Batch](actions/get-batch.md) | `GET /v2/batches/:batchId` | [docs](https://api.print.one/docs/v2#operation/Batch/getBatch) |
| [Get Batch CSV Import Details](actions/get-batch-csv-import-details.md) | `GET /v2/batches/:batchId/orders/csv/:csvId` | [docs](https://api.print.one/docs/v2#operation/Batch/getCsvDetails) |
| [Get Batch Order](actions/get-batch-order.md) | `GET /v2/batches/:batchId/orders/:orderId` | [docs](https://api.print.one/docs/v2#operation/Batch/getBatchOrder) |
| [Get Batch Stats](actions/get-batch-stats.md) | `GET /v2/batches/:batchId/stats` | [docs](https://api.print.one/docs/v2#operation/Batch/getBatchStats) |
| [Get My Company](actions/get-my-company.md) | `GET /v2/companies/me` | [docs](https://api.print.one/docs/v2#operation/getMe) |
| [Get Order](actions/get-order.md) | `GET /v2/orders/:id` | [docs](https://api.print.one/docs/v2#operation/Order/getOrder) |
| [Get Order Preview](actions/get-order-preview.md) | `GET /v2/storage/order/preview/[:orderId]` | [docs](https://api.print.one/docs/v2#operation/Storage/getOrderPreview) |
| [Get Template](actions/get-template.md) | `GET /v2/templates/[:id]/[:version]` | [docs](https://api.print.one/docs/v2#operation/Template/getTemplate) |
| [Get Template Preview](actions/get-template-preview.md) | `GET /v2/storage/template/preview/[:previewId]` | [docs](https://api.print.one/docs/v2#operation/Storage/getTemplatePreview) |
| [Get Template Preview Details](actions/get-template-preview-details.md) | `GET /v2/storage/template/preview/[:previewId]/details` | [docs](https://api.print.one/docs/v2#operation/Storage/getTemplatePreviewDetails) |
| [List Batch Orders](actions/list-batch-orders.md) | `GET /v2/batches/:batchId/orders` | [docs](https://api.print.one/docs/v2#operation/Batch/getOrderList) |
| [List Batches](actions/list-batches.md) | `GET /v2/batches` | [docs](https://api.print.one/docs/v2#operation/Batch/getBatchList) |
| [List Custom Files](actions/list-custom-files.md) | `GET /v2/customfiles` | [docs](https://api.print.one/docs/v2#operation/CustomFiles/getCustomFileList) |
| [List Orders](actions/list-orders.md) | `GET /v2/orders` | [docs](https://api.print.one/docs/v2#operation/Order/getOrderList) |
| [List Supported Countries](actions/list-supported-countries.md) | `GET /v2/countries` | [docs](https://api.print.one/docs/v2#operation/Country/getSupportedCountries) |
| [List Template Versions](actions/list-template-versions.md) | `GET /v2/templates/[:id]/versions` | [docs](https://api.print.one/docs/v2#operation/Template/getTemplateVersions) |
| [List Templates](actions/list-templates.md) | `GET /v2/templates` | [docs](https://api.print.one/docs/v2#operation/Template/getTemplateList) |
| [Update Batch](actions/update-batch.md) | `PATCH /v2/batches/:batchId` | [docs](https://api.print.one/docs/v2#operation/Batch/updateBatch) |
| [Update Template](actions/update-template.md) | `PATCH /v2/templates/[:id]` | [docs](https://api.print.one/docs/v2#operation/Template/updateTemplate) |
| [Upload Custom File](actions/upload-custom-file.md) | `POST /v2/customfiles` | [docs](https://api.print.one/docs/v2#operation/CustomFiles/uploadCustomFile) |
