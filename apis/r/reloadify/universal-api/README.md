# <img src="https://images.mindcloud.co/apps/icons/id-x-d-yy-lzn-logos_1774640821892.jpeg" alt="Reloadify logo" width="28" height="28"> Reloadify: Universal API

Reloadify is a retention marketing platform for ecommerce that helps merchants sync customer, product, order, cart, and review data to power email automation and personalization.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/reloadify/latest
- **Category:** Marketing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.reloadify.com/en
- **Vendor API docs:** https://app.reloadify.com/api-docs/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Languages](actions/list-languages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-languages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Brand

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Brand](actions/create-or-update-brand.md) | PUT | Creates or updates a brand in Reloadify. |
| [Get Brand](actions/get-brand.md) | GET | Retrieves a brand from Reloadify. |
| [List Brands](actions/list-brands.md) | GET | Retrieves brands from Reloadify. |

### Cart

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Shopping Cart](actions/create-or-update-shopping-cart.md) | PUT | Creates or updates a shopping cart in Reloadify. |
| [Get Shopping Cart](actions/get-shopping-cart.md) | GET | Retrieves a shopping cart from Reloadify. |
| [List Shopping Carts](actions/list-shopping-carts.md) | GET | Retrieves shopping carts from Reloadify. |

### Cart Product

| Action | Method | Description |
| --- | --- | --- |
| [Add Product To Cart](actions/add-product-to-cart.md) | PUT | Adds a product to a shopping cart in Reloadify. |
| [List Cart Products](actions/list-cart-products.md) | GET | Retrieves products for a shopping cart in Reloadify. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Category](actions/create-or-update-category.md) | PUT | Creates or updates a category in Reloadify. |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from Reloadify. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from Reloadify. |
| [List Product Categories](actions/list-product-categories.md) | GET | Retrieves product categories from Reloadify. |

### Category Product

| Action | Method | Description |
| --- | --- | --- |
| [Add Product To Category](actions/add-product-to-category.md) | PUT | Adds a product to a category in Reloadify. |

### Custom Attribute

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Custom Attribute](actions/create-or-update-custom-attribute.md) | PUT | Creates or updates a custom attribute in Reloadify. |
| [List Custom Attributes](actions/list-custom-attributes.md) | GET | Retrieves custom attributes from Reloadify. |

### Global Unsubscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Global Unsubscription](actions/create-global-unsubscription.md) | POST | Creates a global unsubscription in Reloadify. |
| [List Global Unsubscribes](actions/list-global-unsubscribes.md) | GET | Retrieves global unsubscribes from Reloadify. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [List Languages](actions/list-languages.md) | GET | Retrieves languages from Reloadify. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Order](actions/create-or-update-order.md) | PUT | Creates or updates an order in Reloadify. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Reloadify. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Reloadify. |

### Order Line

| Action | Method | Description |
| --- | --- | --- |
| [Add Product To Order](actions/add-product-to-order.md) | PUT | Adds a product to an order in Reloadify. |
| [List Order Products](actions/list-order-products.md) | GET | Retrieves products for an order in Reloadify. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Product](actions/create-or-update-product.md) | PUT | Creates or updates a product in Reloadify. |
| [List Brand Products](actions/list-brand-products.md) | GET | Retrieves products for a brand in Reloadify. |

### Product Variants

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Variant](actions/create-or-update-variant.md) | PUT | Creates or updates a product variant in Reloadify. |
| [Get Variant](actions/get-variant.md) | GET | Retrieves a product variant from Reloadify. |
| [List Product Variants](actions/list-product-variants.md) | GET | Retrieves product variants from Reloadify. |
| [List Variants](actions/list-variants.md) | GET | Retrieves product variants from Reloadify. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Reloadify. |
| [List Category Products](actions/list-category-products.md) | GET | Retrieves category products from Reloadify. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Reloadify. |
| [List Relevant Products](actions/list-relevant-products.md) | GET | Retrieves relevant products from Reloadify. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Profile](actions/create-or-update-profile.md) | PUT | Creates or updates a profile in Reloadify by email. |
| [Get Profile](actions/get-profile.md) | GET | Retrieves a profile from Reloadify. |
| [List Profiles](actions/list-profiles.md) | GET | Retrieves profiles from Reloadify. |

### Purchase Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase Event](actions/create-purchase-event.md) | POST | Creates a server-side purchase event in Reloadify. |

### Review

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Review](actions/create-or-update-review.md) | PUT | Creates or updates a review in Reloadify. |
| [Get Review](actions/get-review.md) | GET | Retrieves a review from Reloadify. |
| [List Reviews](actions/list-reviews.md) | GET | Retrieves reviews from Reloadify. |

