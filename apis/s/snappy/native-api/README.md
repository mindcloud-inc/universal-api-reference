# Snappy: Native API Reference

A consolidated summary of Snappy's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://docs.snappy.com/reference
- **API base URL:** `https://api.snappy.com/public-api/v2`

## Authentication

### API Key

Authenticate with a Snappy company API key sent in the X-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.snappy.com/docs/company-level-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `skip` in the query string as the record offset.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Autocomplete Order Address](actions/autocomplete-order-address.md) | `GET /orders/addresses/autocomplete` | [docs](https://docs.snappy.com/reference/autocompleteorderaddress) |
| [Claim Gift](actions/claim-gift.md) | `POST /gifts/{giftId}/claim` | [docs](https://docs.snappy.com/reference/claimgift) |
| [Create Account](actions/create-account.md) | `POST /accounts` | [docs](https://docs.snappy.com/reference/createaccount) |
| [Create API Key](actions/create-api-key.md) | `POST /authentication/apiKeys` | [docs](https://docs.snappy.com/reference/createapikey) |
| [Create Campaign](actions/create-campaign.md) | `POST /campaigns` | [docs](https://docs.snappy.com/reference/createcampaign-1) |
| [Create Demo Gift](actions/create-demo-gift.md) | `POST /gifts/demo` | [docs](https://docs.snappy.com/reference/createdemogift) |
| [Create Gifts](actions/create-gifts.md) | `POST /gifts` | [docs](https://docs.snappy.com/reference/creategifts) |
| [Create Recipient](actions/create-recipient.md) | `POST /recipients` | [docs](https://docs.snappy.com/reference/createrecipient) |
| [Delete API Key](actions/delete-api-key.md) | `DELETE /authentication/apiKeys/{apiKeyId}` | [docs](https://docs.snappy.com/reference/deleteapikey) |
| [Delete Recipient](actions/delete-recipient.md) | `DELETE /recipients/{recipientId}` | [docs](https://docs.snappy.com/reference/deleterecipientbyid) |
| [Expire Gift](actions/expire-gift.md) | `POST /gifts/{giftId}/expire` | [docs](https://docs.snappy.com/reference/expiregift) |
| [Get Account](actions/get-account.md) | `GET /accounts/{accountId}` | [docs](https://docs.snappy.com/reference/getaccount) |
| [Get API Keys](actions/get-api-keys.md) | `GET /authentication/apiKeys` | [docs](https://docs.snappy.com/reference/getapikeys) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/{campaignId}` | [docs](https://docs.snappy.com/reference/getcampaign) |
| [Get Collection Product](actions/get-collection-product.md) | `GET /collections/{collectionId}/products/{productId}` | [docs](https://docs.snappy.com/reference/getcollectionproduct) |
| [Get Estimated Cost](actions/get-estimated-cost.md) | `GET /campaigns/{campaignId}/estimatedCost` | [docs](https://docs.snappy.com/reference/getestimatedcost) |
| [Get Gift](actions/get-gift.md) | `GET /gifts/{giftId}` | [docs](https://docs.snappy.com/reference/getgift) |
| [Get Recipient](actions/get-recipient.md) | `GET /recipients/{recipientId}` | [docs](https://docs.snappy.com/reference/getrecipient) |
| [Get Variant](actions/get-variant.md) | `GET /variants/{variantId}` | [docs](https://docs.snappy.com/reference/getvariantbyid) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://docs.snappy.com/reference/getaccounts) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://docs.snappy.com/reference/getcampaigns) |
| [List Collection Products](actions/list-collection-products.md) | `GET /collections/{collectionId}/products` | [docs](https://docs.snappy.com/reference/getcollectionproducts) |
| [List Collections](actions/list-collections.md) | `GET /collections` | [docs](https://docs.snappy.com/reference/getcollections) |
| [List Gifts](actions/list-gifts.md) | `GET /gifts` | [docs](https://docs.snappy.com/reference/getgifts) |
| [List Product Tags](actions/list-product-tags.md) | `GET /products/tags` | [docs](https://docs.snappy.com/reference/getproducttags) |
| [List Product Variants](actions/list-product-variants.md) | `GET /products/{productId}` | [docs](https://docs.snappy.com/reference/getvariantsbyproductid) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://docs.snappy.com/reference/getproducts) |
| [List Recipients](actions/list-recipients.md) | `GET /recipients` | [docs](https://docs.snappy.com/reference/getrecipients) |
| [Update Campaign](actions/update-campaign.md) | `PATCH /campaigns/{campaignId}` | [docs](https://docs.snappy.com/reference/updatecampaign) |
| [Update Gift](actions/update-gift.md) | `PATCH /gifts/{giftId}` | [docs](https://docs.snappy.com/reference/patchgift) |
| [Update Recipient](actions/update-recipient.md) | `PATCH /recipients/{recipientId}` | [docs](https://docs.snappy.com/reference/updaterecipient) |
| [Validate Order Address](actions/validate-order-address.md) | `POST /orders/addresses/validate` | [docs](https://docs.snappy.com/reference/validateorderaddress) |
