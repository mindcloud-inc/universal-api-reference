# <img src="https://images.mindcloud.co/apps/icons/printful-icon_1775850182425.png" alt="Printful logo" width="28" height="28"> Printful: Universal API

Printful is a print-on-demand and warehousing platform. Use this app to manage stores, products, product templates, orders, files, shipping estimates, webhooks, warehouse products, and reporting through the Printful API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/printful/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 55
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.printful.com
- **Vendor API docs:** https://developers.printful.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Stores](actions/list-stores.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printful/latest/actions/list-stores?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (55)

### Approval Sheet

| Action | Method | Description |
| --- | --- | --- |
| [Create Approval Sheet](actions/create-approval-sheet.md) | POST | Approves a design by creating a Printful approval sheet. |
| [Get Approval Sheets](actions/get-approval-sheets.md) | GET | Retrieves approval sheets from your Printful account. |
| [Submit Approval Sheet Changes](actions/submit-approval-sheet-changes.md) | PUT | Submits changes to a Printful approval sheet. |

### Catalog Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Catalog Product](actions/get-catalog-product.md) | GET | Retrieves a product from the Printful catalog. |
| [List Catalog Products](actions/list-catalog-products.md) | GET | Retrieves products from the Printful catalog. |

### Catalog Variant

| Action | Method | Description |
| --- | --- | --- |
| [Get Catalog Variant](actions/get-catalog-variant.md) | GET | Retrieves a catalog variant from Printful. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | GET | Retrieves a product category from the Printful catalog. |
| [List Categories](actions/list-categories.md) | GET | Retrieves product categories from the Printful catalog. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves supported country codes from Printful. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Add File](actions/add-file.md) | POST | Adds a file to the Printful library. |
| [Get File](actions/get-file.md) | GET | Retrieves a file from the Printful library. |

### Mockup Printfile

| Action | Method | Description |
| --- | --- | --- |
| [Get Mockup Printfiles](actions/get-mockup-printfiles.md) | GET | Retrieves variant printfiles for Printful mockup generation. |

### Mockup Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Mockup Task](actions/create-mockup-task.md) | POST | Creates a mockup generation task in Printful. |
| [Get Mockup Task](actions/get-mockup-task.md) | GET | Retrieves a Printful mockup generation task result. |

### Mockup Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Mockup Templates](actions/get-mockup-templates.md) | GET | Retrieves layout templates for Printful mockup generation. |

### Oauth Scope

| Action | Method | Description |
| --- | --- | --- |
| [List OAuth Scopes](actions/list-o-auth-scopes.md) | GET | Retrieves available OAuth scopes for a Printful token. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Order](actions/cancel-order.md) | DELETE | Cancels an existing order in Printful. |
| [Confirm Order](actions/confirm-order.md) | PUT | Confirms a draft Printful order for fulfillment. |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Printful. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from your Printful account. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from your Printful account. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in Printful. |

### Order Cost Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Estimate Order Costs](actions/estimate-order-costs.md) | GET | Estimates costs for a Printful order draft. |

### Packing Slip

| Action | Method | Description |
| --- | --- | --- |
| [Change Packing Slip](actions/change-packing-slip.md) | PUT | Updates the packing slip for a Printful store. |

### Product Size Guide

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Size Guide](actions/get-product-size-guide.md) | GET | Retrieves a size guide for a Printful catalog product. |

### Product Template

| Action | Method | Description |
| --- | --- | --- |
| [Delete Product Template](actions/delete-product-template.md) | DELETE | Deletes a product template from Printful. |
| [Get Product Template](actions/get-product-template.md) | GET | Retrieves a product template from your Printful account. |
| [List Product Templates](actions/list-product-templates.md) | GET | Retrieves product templates from your Printful account. |

### Shipping Rate

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Shipping Rates](actions/calculate-shipping-rates.md) | GET | Calculates shipping rates for a Printful shipment. |

### Statistics Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Statistics](actions/get-statistics.md) | GET | Retrieves account statistics from your Printful account. |

### Store

| Action | Method | Description |
| --- | --- | --- |
| [Get Store](actions/get-store.md) | GET | Retrieves a store from your Printful account. |
| [List Stores](actions/list-stores.md) | GET | Retrieves stores available in your Printful account. |

### Store Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Store Product](actions/create-store-product.md) | POST | Creates a new sync product in a Printful store. |
| [Delete Store Product](actions/delete-store-product.md) | DELETE | Deletes a sync product from a Printful store. |
| [Get Store Product](actions/get-store-product.md) | GET | Retrieves a sync product from a Printful store. |
| [List Store Products](actions/list-store-products.md) | GET | Retrieves sync products from a Printful store. |
| [Update Store Product](actions/update-store-product.md) | PUT | Updates a sync product in a Printful store. |

### Store Variant

| Action | Method | Description |
| --- | --- | --- |
| [Create Store Variant](actions/create-store-variant.md) | POST | Creates a new sync variant in a Printful store. |
| [Delete Store Variant](actions/delete-store-variant.md) | DELETE | Deletes a sync variant from a Printful store. |
| [Get Store Variant](actions/get-store-variant.md) | GET | Retrieves a sync variant from a Printful store. |
| [Update Store Variant](actions/update-store-variant.md) | PUT | Updates a sync variant in a Printful store. |

### Sync Product

| Action | Method | Description |
| --- | --- | --- |
| [Delete Sync Product](actions/delete-sync-product.md) | DELETE | Deletes a synced product from your Printful integrations. |
| [Get Sync Product](actions/get-sync-product.md) | GET | Retrieves a synced product from your Printful integrations. |
| [List Sync Products](actions/list-sync-products.md) | GET | Retrieves synced products from your Printful integrations. |

### Sync Variant

| Action | Method | Description |
| --- | --- | --- |
| [Delete Sync Variant](actions/delete-sync-variant.md) | DELETE | Deletes a synced variant from your Printful integrations. |
| [Get Sync Variant](actions/get-sync-variant.md) | GET | Retrieves a synced variant from your Printful integrations. |
| [Update Sync Variant](actions/update-sync-variant.md) | PUT | Updates a synced variant in your Printful integrations. |

### Tax Country

| Action | Method | Description |
| --- | --- | --- |
| [List Tax Countries](actions/list-tax-countries.md) | GET | Retrieves countries available for Printful tax calculations. |

### Tax Rate

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Tax Rates](actions/calculate-tax-rates.md) | GET | Calculates tax rates for a Printful order. |

### Thread Color Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Suggest Thread Colors](actions/suggest-thread-colors.md) | GET | Retrieves suggested thread colors from an image in Printful. |

### Warehouse Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Warehouse Product](actions/get-warehouse-product.md) | GET | Retrieves a warehouse product from your Printful account. |
| [List Warehouse Products](actions/list-warehouse-products.md) | GET | Retrieves warehouse products from your Printful account. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates webhook configuration in your Printful account. |
| [Disable Webhook](actions/disable-webhook.md) | DELETE | Disables webhook support in your Printful account. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhook configuration from your Printful account. |

