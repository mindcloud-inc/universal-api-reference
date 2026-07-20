# Rakuten Advertising: Native API Reference

A consolidated summary of Rakuten Advertising's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis
- **API base URL:** `https://api.linksynergy.com`

## Authentication

### API access token (Applications page)

Paste the API access token generated from Rakuten Advertising Applications. Do not use the Web service token from APIs > Manage Tokens. In Applications, click Generate Token and enter your numerical publisher SID as the token scope.

### Credentials

- **Access Token:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.rakutenadvertising.com/guides/access_tokens)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `order_by`. Use `asc` for ascending order and `dsc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create deep link](actions/create-deep-link.md) | `POST /v1/links/deep_links` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/deep_link) |
| [Create postback](actions/create-postback.md) | `POST /v1/postback` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/postback) |
| [Delete postback](actions/delete-postback.md) | `DELETE /v1/postback/{publisherId}` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/postback) |
| [Get advertiser](actions/get-advertiser.md) | `GET /v2/advertisers/{advertiserId}` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/advertisers) |
| [Get banner links](actions/get-banner-links.md) | `GET /linklocator/1.0/getBannerLinks/{advertiserId}/{categoryId}/{linkStartDate}/{linkEndDate}/{bannerSizeCode}/{campaignId}/{page}` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/link_locator) |
| [Get commissioning list](actions/get-commissioning-list.md) | `GET /v1/commissioninglists/{listId}` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/commissioning_lists) |
| [Get creative categories](actions/get-creative-categories.md) | `GET /linklocator/1.0/getCreativeCategories/{advertiserId}` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/link_locator) |
| [Get DRM links](actions/get-drm-links.md) | `GET /linklocator/1.0/getDRMLinks/{advertiserId}/{categoryId}/{linkStartDate}/{linkEndDate}/{campaignId}/{page}` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/link_locator) |
| [Get invoice item report](actions/get-invoice-item-report.md) | `GET /advancedreports/1.0` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/advanced_reports) |
| [Get invoice report](actions/get-invoice-report.md) | `GET /advancedreports/1.0` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/advanced_reports) |
| [Get merchant by ID](actions/get-merchant-by-id.md) | `GET /linklocator/1.0/getMerchByID/{advertiserId}` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/link_locator) |
| [Get merchants by application status](actions/get-merchants-by-application-status.md) | `GET /linklocator/1.0/getMerchByAppStatus/{applicationStatus}` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/link_locator) |
| [Get merchants by category](actions/get-merchants-by-category.md) | `GET /linklocator/1.0/getMerchByCategory/{categoryId}` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/link_locator) |
| [Get merchants by name](actions/get-merchants-by-name.md) | `GET /linklocator/1.0/getMerchByName/{advertiserName}` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/link_locator) |
| [Get offer](actions/get-offer.md) | `GET /v1/offers/{goid}` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/offers) |
| [Get partnership](actions/get-partnership.md) | `GET /v1/partnerships/{advertiserId}` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/partnerships) |
| [Get payment report](actions/get-payment-report.md) | `GET /advancedreports/1.0` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/advanced_reports) |
| [Get postback](actions/get-postback.md) | `GET /v1/postback/{publisherId}` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/postback) |
| [Get signature orders payment report](actions/get-signature-orders-payment-report.md) | `GET /advancedreports/1.0` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/advanced_reports) |
| [Get text links](actions/get-text-links.md) | `GET /linklocator/1.0/getTextLinks/{advertiserId}/{categoryId}/{linkStartDate}/{linkEndDate}/{campaignId}/{page}` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/link_locator) |
| [List advertisers](actions/list-advertisers.md) | `GET /v2/advertisers` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/advertisers) |
| [List commissioning lists](actions/list-commissioning-lists.md) | `GET /v1/commissioninglists` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/commissioning_lists) |
| [List contributed conversions](actions/list-contributed-conversions.md) | `GET /v1/publishers/contributed-conversions` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis) |
| [List coupon metadata](actions/list-coupon-metadata.md) | `GET /coupon/1.0` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/coupon/reference) |
| [List coupons](actions/list-coupons.md) | `GET /coupon/1.0` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/coupon) |
| [List offers](actions/list-offers.md) | `GET /v1/offers` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/offers) |
| [List partnerships](actions/list-partnerships.md) | `GET /v1/partnerships` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/partnerships) |
| [List transactions](actions/list-transactions.md) | `GET /events/1.0/transactions` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/events) |
| [Run advanced report](actions/run-advanced-report.md) | `GET /advancedreports/1.0` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/advanced_reports) |
| [Run advertiser advanced report](actions/run-advertiser-advanced-report.md) | `GET /advancedreports/1.0` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/advanced_reports) |
| [Run localized advanced report](actions/run-localized-advanced-report.md) | `GET /advancedreports/1.0` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/advanced_reports) |
| [Run network advanced report](actions/run-network-advanced-report.md) | `GET /advancedreports/1.0` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/advanced_reports) |
| [Search advertisers](actions/search-advertisers.md) | `GET /advertisersearch/1.0` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/advertiser_search) |
| [Search products](actions/search-products.md) | `GET /productsearch/1.0` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/product_search) |
| [Update postback](actions/update-postback.md) | `PUT /v1/postback/{sid}` | [docs](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/postback) |
