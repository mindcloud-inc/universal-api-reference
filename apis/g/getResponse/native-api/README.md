# GetResponse: Native API Reference

A consolidated summary of GetResponse's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://apireference.getresponse.com/
- **OpenAPI specification:** https://apireference.getresponse.com/open-api.json
- **API base URL:** `https://api.getresponse.com/v3`

## Authentication

### OAuth 2.0

Authenticate with GetResponse using OAuth 2.0 Authorization Code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.getresponse.com/oauth2_authorize.html to approve access.
2. Exchange the returned authorization code with a POST request to https://api.getresponse.com/v3/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.getresponse.com/v3/token.

[Official authentication documentation](https://apidocs.getresponse.com/v3/#section/Authentication/Using-OAuth-2.0)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `perPage` in the query string to set the page size (default 100; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://apireference.getresponse.com/#operation/createContact) |
| [Create Product](actions/create-product.md) | `POST /shops/:shopId/products` | [docs](https://apireference.getresponse.com/#operation/createProduct) |
| [Create Shop](actions/create-shop.md) | `POST /shops` | [docs](https://apireference.getresponse.com/#operation/createShop) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:contactId` | [docs](https://apireference.getresponse.com/#operation/deleteContact) |
| [Delete Product](actions/delete-product.md) | `DELETE /shops/:shopId/products/:productId` | [docs](https://apireference.getresponse.com/#operation/deleteProduct) |
| [Delete Shop](actions/delete-shop.md) | `DELETE /shops/:shopId` | [docs](https://apireference.getresponse.com/#operation/deleteShop) |
| [Get Account](actions/get-account.md) | `GET /accounts` | [docs](https://apireference.getresponse.com/#operation/getAccount) |
| [Get Account Login History](actions/get-account-login-history.md) | `GET /accounts/login-history` | [docs](https://apireference.getresponse.com/#operation/getAccountLoginHistory) |
| [Get Campaign Statistics Balance](actions/get-campaign-statistics-balance.md) | `GET /campaigns/statistics/balance` | [docs](https://apireference.getresponse.com/#operation/getCampaignStatisticsBalance) |
| [Get Campaign Statistics List Size](actions/get-campaign-statistics-list-size.md) | `GET /campaigns/statistics/list-size` | [docs](https://apireference.getresponse.com/#operation/getCampaignStatisticsListSize) |
| [Get Campaign Statistics Locations](actions/get-campaign-statistics-locations.md) | `GET /campaigns/statistics/locations` | [docs](https://apireference.getresponse.com/#operation/getCampaignStatisticsLocations) |
| [Get Campaign Statistics Origins](actions/get-campaign-statistics-origins.md) | `GET /campaigns/statistics/origins` | [docs](https://apireference.getresponse.com/#operation/getCampaignStatisticsOrigins) |
| [Get Campaign Statistics Removals](actions/get-campaign-statistics-removals.md) | `GET /campaigns/statistics/removals` | [docs](https://apireference.getresponse.com/#operation/getCampaignStatisticsRemovals) |
| [Get Campaign Statistics Subscriptions](actions/get-campaign-statistics-subscriptions.md) | `GET /campaigns/statistics/subscriptions` | [docs](https://apireference.getresponse.com/#operation/getCampaignStatisticsSubscriptions) |
| [Get Campaign Statistics Summary](actions/get-campaign-statistics-summary.md) | `GET /campaigns/statistics/summary` | [docs](https://apireference.getresponse.com/#operation/getCampaignStatisticsSummary) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contactId` | [docs](https://apireference.getresponse.com/#operation/getContactById) |
| [Get Newsletter Statistics](actions/get-newsletter-statistics.md) | `GET /newsletters/statistics` | [docs](https://apireference.getresponse.com/#operation/getNewsletterStatisticsCollection) |
| [Get Product](actions/get-product.md) | `GET /shops/:shopId/products/:productId` | [docs](https://apireference.getresponse.com/#operation/getProductById) |
| [Get Sending Limits](actions/get-sending-limits.md) | `GET /accounts/sending-limits` | [docs](https://apireference.getresponse.com/#operation/getSendingLimits) |
| [Get Shop](actions/get-shop.md) | `GET /shops/:shopId` | [docs](https://apireference.getresponse.com/#operation/getShopById) |
| [Get Tracking Snippets](actions/get-tracking-snippets.md) | `GET /tracking` | [docs](https://apireference.getresponse.com/#operation/getTracking) |
| [List Addresses](actions/list-addresses.md) | `GET /addresses` | [docs](https://apireference.getresponse.com/#operation/getAddressList) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://apireference.getresponse.com/#operation/getCampaignList) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://apireference.getresponse.com/#operation/getContactList) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /custom-fields` | [docs](https://apireference.getresponse.com/#operation/getCustomFieldList) |
| [List Facebook Pixels](actions/list-facebook-pixels.md) | `GET /tracking/facebook-pixels` | [docs](https://apireference.getresponse.com/#operation/getFacebookPixelList) |
| [List From Fields](actions/list-from-fields.md) | `GET /from-fields` | [docs](https://apireference.getresponse.com/#operation/getFromFieldList) |
| [List Industries](actions/list-industries.md) | `GET /accounts/industries` | [docs](https://apireference.getresponse.com/#operation/getIndustries) |
| [List Newsletters](actions/list-newsletters.md) | `GET /newsletters` | [docs](https://apireference.getresponse.com/#operation/getNewsletterList) |
| [List Products](actions/list-products.md) | `GET /shops/:shopId/products` | [docs](https://apireference.getresponse.com/#operation/getProductList) |
| [List Search Contacts](actions/list-search-contacts.md) | `GET /search-contacts` | [docs](https://apireference.getresponse.com/#operation/getSearchContactsList) |
| [List Shops](actions/list-shops.md) | `GET /shops` | [docs](https://apireference.getresponse.com/#operation/getShopList) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://apireference.getresponse.com/#operation/getTagsList) |
| [List Timezones](actions/list-timezones.md) | `GET /accounts/timezones` | [docs](https://apireference.getresponse.com/#operation/getTimezones) |
| [List Websites](actions/list-websites.md) | `GET /websites` | [docs](https://apireference.getresponse.com/#operation/getWebsitesList) |
| [Update Contact](actions/update-contact.md) | `POST /contacts/:contactId` | [docs](https://apireference.getresponse.com/#operation/updateContact) |
| [Update Product](actions/update-product.md) | `POST /shops/:shopId/products/:productId` | [docs](https://apireference.getresponse.com/#operation/updateProduct) |
| [Update Shop](actions/update-shop.md) | `POST /shops/:shopId` | [docs](https://apireference.getresponse.com/#operation/updateShop) |
| [Upsert Product Categories](actions/upsert-product-categories.md) | `POST /shops/:shopId/products/:productId/categories` | [docs](https://apireference.getresponse.com/#operation/upsertProductCategories) |
| [Upsert Product Meta Fields](actions/upsert-product-meta-fields.md) | `POST /shops/:shopId/products/:productId/meta-fields` | [docs](https://apireference.getresponse.com/#operation/upsertMetaFields) |
