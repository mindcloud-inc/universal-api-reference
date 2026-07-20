# Reloadify: Native API Reference

A consolidated summary of Reloadify's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://app.reloadify.com/api-docs/index.html
- **OpenAPI specification:** https://app.reloadify.com/api/v2/swagger_doc
- **API base URL:** `https://api.reloadify.com/api`

## Authentication

### OAuth2 Client Credentials

Use Reloadify OAuth2 client credentials to exchange a client ID and client secret for a bearer token.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.reloadify.com/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://help.reloadify.com/en/articles/7135513-reloadify-api-installation-guide)

## API conventions

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 10; maximum 250). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Product To Cart](actions/add-product-to-cart.md) | `PUT /v2/languages/:language_id/shopping_carts/:shopping_cart_id/products/:product_id` | [docs](https://app.reloadify.com/api-docs/index.html#/shopping_carts/putV2LanguagesLanguageIdShoppingCartsShoppingCartIdProductsProductId) |
| [Add Product To Category](actions/add-product-to-category.md) | `PUT /v2/languages/:language_id/products/:product_id/categories/:category_id` | [docs](https://app.reloadify.com/api-docs/index.html#/products/putV2LanguagesLanguageIdProductsProductIdCategoriesCategoryId) |
| [Add Product To Order](actions/add-product-to-order.md) | `PUT /v2/languages/:language_id/orders/:order_id/products/:product_id` | [docs](https://app.reloadify.com/api-docs/index.html#/orders/putV2LanguagesLanguageIdOrdersOrderIdProductsProductId) |
| [Create Global Unsubscription](actions/create-global-unsubscription.md) | `PUT /v2/languages/:language_id/global_unsubscribes` | [docs](https://app.reloadify.com/api-docs/index.html#/global_unsubscribes/putV2LanguagesLanguageIdGlobalUnsubscribes) |
| [Create Or Update Brand](actions/create-or-update-brand.md) | `PUT /v2/languages/:language_id/brands` | [docs](https://app.reloadify.com/api-docs/index.html#/brands/putV2LanguagesLanguageIdBrands) |
| [Create Or Update Category](actions/create-or-update-category.md) | `PUT /v2/languages/:language_id/categories` | [docs](https://app.reloadify.com/api-docs/index.html#/categories/putV2LanguagesLanguageIdCategories) |
| [Create Or Update Custom Attribute](actions/create-or-update-custom-attribute.md) | `PUT /v2/custom_attributes` | [docs](https://app.reloadify.com/api-docs/index.html#/custom_attributes/putV2CustomAttributes) |
| [Create Or Update Order](actions/create-or-update-order.md) | `PUT /v2/languages/:language_id/orders` | [docs](https://app.reloadify.com/api-docs/index.html#/orders/putV2LanguagesLanguageIdOrders) |
| [Create Or Update Product](actions/create-or-update-product.md) | `PUT /v2/languages/:language_id/products` | [docs](https://app.reloadify.com/api-docs/index.html#/products/putV2LanguagesLanguageIdProducts) |
| [Create Or Update Profile](actions/create-or-update-profile.md) | `PUT /v2/languages/:language_id/profiles` | [docs](https://app.reloadify.com/api-docs/index.html#/profiles/putV2LanguagesLanguageIdProfiles) |
| [Create Or Update Review](actions/create-or-update-review.md) | `PUT /v2/languages/:language_id/reviews` | [docs](https://app.reloadify.com/api-docs/index.html#/reviews/putV2LanguagesLanguageIdReviews) |
| [Create Or Update Shopping Cart](actions/create-or-update-shopping-cart.md) | `PUT /v2/languages/:language_id/shopping_carts` | [docs](https://app.reloadify.com/api-docs/index.html#/shopping_carts/putV2LanguagesLanguageIdShoppingCarts) |
| [Create Or Update Variant](actions/create-or-update-variant.md) | `PUT /v2/languages/:language_id/variants` | [docs](https://app.reloadify.com/api-docs/index.html#/variants/putV2LanguagesLanguageIdVariants) |
| [Create Purchase Event](actions/create-purchase-event.md) | `PUT /v2/languages/:language_id/purchase_events` | [docs](https://app.reloadify.com/api-docs/index.html#/purchase_events/putV2LanguagesLanguageIdPurchaseEvents) |
| [Get Brand](actions/get-brand.md) | `GET /v2/languages/:language_id/brands/:brand_id` | [docs](https://app.reloadify.com/api-docs/index.html#/brands/getV2LanguagesLanguageIdBrandsBrandId) |
| [Get Category](actions/get-category.md) | `GET /v2/languages/:language_id/categories/:category_id` | [docs](https://app.reloadify.com/api-docs/index.html#/categories/getV2LanguagesLanguageIdCategoriesCategoryId) |
| [Get Order](actions/get-order.md) | `GET /v2/languages/:language_id/orders/:order_id` | [docs](https://app.reloadify.com/api-docs/index.html#/orders/getV2LanguagesLanguageIdOrdersOrderId) |
| [Get Product](actions/get-product.md) | `GET /v2/languages/:language_id/products/:product_id` | [docs](https://app.reloadify.com/api-docs/index.html#/products/getV2LanguagesLanguageIdProductsProductId) |
| [Get Profile](actions/get-profile.md) | `GET /v2/languages/:language_id/profiles/:profile_id` | [docs](https://app.reloadify.com/api-docs/index.html#/profiles/getV2LanguagesLanguageIdProfilesProfileId) |
| [Get Review](actions/get-review.md) | `GET /v2/languages/:language_id/reviews/:review_id` | [docs](https://app.reloadify.com/api-docs/index.html#/reviews/getV2LanguagesLanguageIdReviewsReviewId) |
| [Get Shopping Cart](actions/get-shopping-cart.md) | `GET /v2/languages/:language_id/shopping_carts/:shopping_cart_id` | [docs](https://app.reloadify.com/api-docs/index.html#/shopping_carts/getV2LanguagesLanguageIdShoppingCartsShoppingCartId) |
| [Get Variant](actions/get-variant.md) | `GET /v2/languages/:language_id/variants/:variant_id` | [docs](https://app.reloadify.com/api-docs/index.html#/variants/getV2LanguagesLanguageIdVariantsVariantId) |
| [List Brand Products](actions/list-brand-products.md) | `GET /v2/languages/:language_id/brands/:brand_id/products` | [docs](https://app.reloadify.com/api-docs/index.html#/brands/getV2LanguagesLanguageIdBrandsBrandIdProducts) |
| [List Brands](actions/list-brands.md) | `GET /v2/languages/:language_id/brands` | [docs](https://app.reloadify.com/api-docs/index.html#/brands/getV2LanguagesLanguageIdBrands) |
| [List Cart Products](actions/list-cart-products.md) | `GET /v2/languages/:language_id/shopping_carts/:shopping_cart_id/products` | [docs](https://app.reloadify.com/api-docs/index.html#/shopping_carts/getV2LanguagesLanguageIdShoppingCartsShoppingCartIdProducts) |
| [List Categories](actions/list-categories.md) | `GET /v2/languages/:language_id/categories` | [docs](https://app.reloadify.com/api-docs/index.html#/categories/getV2LanguagesLanguageIdCategories) |
| [List Category Products](actions/list-category-products.md) | `GET /v2/languages/:language_id/categories/:category_id/products` | [docs](https://app.reloadify.com/api-docs/index.html#/categories/getV2LanguagesLanguageIdCategoriesCategoryIdProducts) |
| [List Custom Attributes](actions/list-custom-attributes.md) | `GET /v2/custom_attributes` | [docs](https://app.reloadify.com/api-docs/index.html#/custom_attributes/getV2CustomAttributes) |
| [List Global Unsubscribes](actions/list-global-unsubscribes.md) | `GET /v2/languages/:language_id/global_unsubscribes` | [docs](https://app.reloadify.com/api-docs/index.html#/global_unsubscribes/getV2LanguagesLanguageIdGlobalUnsubscribes) |
| [List Languages](actions/list-languages.md) | `GET /v2/languages` | [docs](https://app.reloadify.com/api-docs/index.html#/languages/getV2Languages) |
| [List Order Products](actions/list-order-products.md) | `GET /v2/languages/:language_id/orders/:order_id/products` | [docs](https://app.reloadify.com/api-docs/index.html#/orders/getV2LanguagesLanguageIdOrdersOrderIdProducts) |
| [List Orders](actions/list-orders.md) | `GET /v2/languages/:language_id/orders` | [docs](https://app.reloadify.com/api-docs/index.html#/orders/getV2LanguagesLanguageIdOrders) |
| [List Product Categories](actions/list-product-categories.md) | `GET /v2/languages/:language_id/products/:product_id/categories` | [docs](https://app.reloadify.com/api-docs/index.html#/products/getV2LanguagesLanguageIdProductsProductIdCategories) |
| [List Product Variants](actions/list-product-variants.md) | `GET /v2/languages/:language_id/products/:product_id/variants` | [docs](https://app.reloadify.com/api-docs/index.html#/products/getV2LanguagesLanguageIdProductsProductIdVariants) |
| [List Products](actions/list-products.md) | `GET /v2/languages/:language_id/products` | [docs](https://app.reloadify.com/api-docs/index.html#/products/getV2LanguagesLanguageIdProducts) |
| [List Profiles](actions/list-profiles.md) | `GET /v2/languages/:language_id/profiles` | [docs](https://app.reloadify.com/api-docs/index.html#/profiles/getV2LanguagesLanguageIdProfiles) |
| [List Relevant Products](actions/list-relevant-products.md) | `GET /v2/languages/:language_id/products/:product_id/relevant_products` | [docs](https://app.reloadify.com/api-docs/index.html#/products/getV2LanguagesLanguageIdProductsProductIdRelevantProducts) |
| [List Reviews](actions/list-reviews.md) | `GET /v2/languages/:language_id/reviews` | [docs](https://app.reloadify.com/api-docs/index.html#/reviews/getV2LanguagesLanguageIdReviews) |
| [List Shopping Carts](actions/list-shopping-carts.md) | `GET /v2/languages/:language_id/shopping_carts` | [docs](https://app.reloadify.com/api-docs/index.html#/shopping_carts/getV2LanguagesLanguageIdShoppingCarts) |
| [List Variants](actions/list-variants.md) | `GET /v2/languages/:language_id/variants` | [docs](https://app.reloadify.com/api-docs/index.html#/variants/getV2LanguagesLanguageIdVariants) |
