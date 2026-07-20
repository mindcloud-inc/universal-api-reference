# ShopWired: Native API Reference

A consolidated summary of ShopWired's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://shopwired.readme.io
- **API base URL:** `https://api.ecommerceapi.uk/v1`

## Authentication

### Basic Auth

Use HTTP Basic authentication. The ShopWired API Key is the username and the API Secret is the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://help.shopwired.io/api/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `count` in the query string to set the page size (default 50; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get a specific brand](actions/get-brand-by-id.md) | `GET /brands/{id}` | [docs](https://shopwired.readme.io/reference/getbrandbyid) |
| [Get total brand count](actions/get-brand-count.md) | `GET /brands/count` | [docs](https://shopwired.readme.io/reference/getbrandcount) |
| [Retrieve business details](actions/get-business.md) | `GET /business` | [docs](https://shopwired.readme.io/reference/getbusiness) |
| [Get a specific category](actions/get-category-by-id.md) | `GET /categories/{id}` | [docs](https://shopwired.readme.io/reference/getcategorybyid) |
| [Get total category count](actions/get-category-count.md) | `GET /categories/count` | [docs](https://shopwired.readme.io/reference/getcategorycount) |
| [Get a specific country](actions/get-country-by-id.md) | `GET /countries/{id}` | [docs](https://shopwired.readme.io/reference/getcountrybyid) |
| [Get a specific customer](actions/get-customer-by-id.md) | `GET /customers/{id}` | [docs](https://shopwired.readme.io/reference/getcustomerbyid) |
| [Get total customer count](actions/get-customer-count.md) | `GET /customers/count` | [docs](https://shopwired.readme.io/reference/getcustomercount) |
| [Get total filter group count](actions/get-filter-group-count.md) | `GET /filter-groups/count` | [docs](https://shopwired.readme.io/reference/getfiltergroupcount) |
| [Get an incomplete order by ID](actions/get-incomplete-order.md) | `GET /incomplete-orders/{id}` | [docs](https://shopwired.readme.io/reference/getincompleteorder) |
| [Get total incomplete order count](actions/get-incomplete-order-count.md) | `GET /incomplete-orders/count` | [docs](https://shopwired.readme.io/reference/getincompleteordercount) |
| [Get a specific newsletter subscriber](actions/get-newsletter-subscriber.md) | `GET /newsletter-subscribers/{id}` | [docs](https://shopwired.readme.io/reference/getnewslettersubscriber) |
| [Get an order by ID](actions/get-order.md) | `GET /orders/{id}` | [docs](https://shopwired.readme.io/reference/getorder) |
| [Get order count](actions/get-order-count.md) | `GET /orders/count` | [docs](https://shopwired.readme.io/reference/getordercount) |
| [Get a single product](actions/get-product-by-id.md) | `GET /products/{id}` | [docs](https://shopwired.readme.io/reference/getproductbyid) |
| [Get a product choice](actions/get-product-choice.md) | `GET /products/{product_id}/choices/{id}` | [docs](https://shopwired.readme.io/reference/getproductchoice) |
| [Get a product option](actions/get-product-option-by-id.md) | `GET /products/{product_id}/options/{id}` | [docs](https://shopwired.readme.io/reference/getproductoptionbyid) |
| [Get a specific product variation](actions/get-product-variation-by-id.md) | `GET /products/{product_id}/variations/{id}` | [docs](https://shopwired.readme.io/reference/getproductvariationbyid) |
| [Retrieve stock quantity](actions/get-stock.md) | `GET /stock` | [docs](https://shopwired.readme.io/reference/getstock) |
| [List active brands](actions/list-brands.md) | `GET /brands` | [docs](https://shopwired.readme.io/reference/listbrands) |
| [List business features](actions/list-business-features.md) | `GET /business/features` | [docs](https://shopwired.readme.io/reference/listbusinessfeatures) |
| [List categories](actions/list-categories.md) | `GET /categories` | [docs](https://shopwired.readme.io/reference/listcategories) |
| [List countries](actions/list-countries.md) | `GET /countries` | [docs](https://shopwired.readme.io/reference/listcountries) |
| [List customers](actions/list-customers.md) | `GET /customers` | [docs](https://shopwired.readme.io/reference/listcustomers) |
| [List filter groups](actions/list-filter-groups.md) | `GET /filter-groups` | [docs](https://shopwired.readme.io/reference/listfiltergroups) |
| [List incomplete orders](actions/list-incomplete-orders.md) | `GET /incomplete-orders` | [docs](https://shopwired.readme.io/reference/listincompleteorders) |
| [List newsletter subscribers](actions/list-newsletter-subscribers.md) | `GET /newsletter-subscribers` | [docs](https://shopwired.readme.io/reference/listnewslettersubscribers) |
| [List order statuses](actions/list-order-statuses.md) | `GET /order-statuses` | [docs](https://shopwired.readme.io/reference/listorderstatuses) |
| [List orders](actions/list-orders.md) | `GET /orders` | [docs](https://shopwired.readme.io/reference/listorders) |
| [List external payment methods](actions/list-payment-methods.md) | `GET /payment-methods` | [docs](https://shopwired.readme.io/reference/listpaymentmethods) |
| [List product choices](actions/list-product-choices.md) | `GET /products/{product_id}/choices` | [docs](https://shopwired.readme.io/reference/listproductchoices) |
| [List product customisation fields](actions/list-product-customization-fields.md) | `GET /products/{product_id}/customization-fields` | [docs](https://shopwired.readme.io/reference/listproductcustomizationfields) |
| [List product extras](actions/list-product-extras.md) | `GET /products/{product_id}/extras` | [docs](https://shopwired.readme.io/reference/listproductextras) |
| [List product images](actions/list-product-images.md) | `GET /products/{product_id}/images` | [docs](https://shopwired.readme.io/reference/listproductimages) |
| [List product options](actions/list-product-options.md) | `GET /products/{product_id}/options` | [docs](https://shopwired.readme.io/reference/listproductoptions) |
| [List product reviews](actions/list-product-reviews.md) | `GET /products/{product_id}/reviews` | [docs](https://shopwired.readme.io/reference/listproductreviews) |
| [List product variations](actions/list-product-variations.md) | `GET /products/{product_id}/variations` | [docs](https://shopwired.readme.io/reference/listproductvariations) |
| [List products](actions/list-products.md) | `GET /products` | [docs](https://shopwired.readme.io/reference/listproducts) |
| [Search for orders](actions/search-orders.md) | `GET /orders/search` | [docs](https://shopwired.readme.io/reference/searchorders) |
| [Search products](actions/search-products.md) | `GET /products/search` | [docs](https://shopwired.readme.io/reference/searchproducts) |
