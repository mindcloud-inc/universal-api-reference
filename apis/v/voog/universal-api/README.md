# <img src="https://images.mindcloud.co/apps/icons/voog-logo-square-black-text_1774977634312.png" alt="Voog logo" width="28" height="28"> Voog: Universal API

Manage Voog sites, content, assets, webhooks, users, and ecommerce resources through the Voog Site API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/voog/latest
- **Category:** Website & App Building / CMS
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.voog.com
- **Vendor API docs:** https://www.voog.com/developers/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List My Sites](actions/list-my-sites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voog/latest/actions/list-my-sites?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Article

| Action | Method | Description |
| --- | --- | --- |
| [Create Article](actions/create-article.md) | POST | Creates a new article in the current Voog site. |
| [Delete Article](actions/delete-article.md) | DELETE | Deletes an existing article from the current Voog site. |
| [Get Article](actions/get-article.md) | GET | Retrieves an article from the current Voog site. |
| [List Articles](actions/list-articles.md) | GET | Retrieves articles for the current Voog site. |
| [Update Article](actions/update-article.md) | PUT | Updates an existing article in the current Voog site. |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Confirm Asset Upload](actions/confirm-asset-upload.md) | PUT | Confirms an asset upload in the current Voog site. |
| [Create Asset](actions/create-asset.md) | POST | Creates a new asset in the current Voog site. |
| [Delete Asset](actions/delete-asset.md) | DELETE | Deletes an existing asset from the current Voog site. |
| [Get Asset](actions/get-asset.md) | GET | Retrieves an asset from the current Voog site. |
| [List Assets](actions/list-assets.md) | GET | Retrieves assets for the current Voog site. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a new category in the current Voog store. |
| [Delete Category](actions/delete-category.md) | DELETE | Deletes an existing category from the current Voog store. |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from the current Voog store. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories for the current Voog store. |
| [Update Category](actions/update-category.md) | PUT | Updates an existing category in the current Voog store. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from the current Voog store. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders for the current Voog store. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in the current Voog store. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | POST | Creates a new page in the current Voog site. |
| [Delete Page](actions/delete-page.md) | DELETE | Deletes an existing page from the current Voog site. |
| [Duplicate Page](actions/duplicate-page.md) | POST | Duplicates a page with its content in Voog. |
| [Get Page](actions/get-page.md) | GET | Retrieves a page from the current Voog site. |
| [List Pages](actions/list-pages.md) | GET | Retrieves pages for the current Voog site. |
| [Update Page](actions/update-page.md) | PUT | Updates an existing page in the current Voog site. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in the current Voog store. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from the current Voog store. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from the current Voog store. |
| [List Products](actions/list-products.md) | GET | Retrieves products for the current Voog store. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in the current Voog store. |

### Shipping Method

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Shipping Method](actions/get-order-shipping-method.md) | GET | Retrieves the shipping method for a Voog order. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [List My Sites](actions/list-my-sites.md) | GET | Retrieves all available sites from your Voog account. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create Site User](actions/create-site-user.md) | POST | Creates a new site user for protected pages in Voog. |
| [Delete Site User](actions/delete-site-user.md) | DELETE | Deletes an existing site user from the current Voog site. |
| [Get Site User](actions/get-site-user.md) | GET | Retrieves a site user from the current Voog site. |
| [List Site Users](actions/list-site-users.md) | GET | Retrieves site users for the current Voog site. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in the current Voog site. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from the current Voog site. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from the current Voog site. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks for the current Voog site. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in the current Voog site. |

