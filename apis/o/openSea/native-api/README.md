# OpenSea: Native API Reference

A consolidated summary of OpenSea's API configuration and 50 documented operations, with links to official documentation.

- **Official docs:** https://docs.opensea.io/reference/api-overview
- **OpenAPI specification:** https://dash.readme.com/api/v1/api-registry/5rn7i1jmnxh54a3
- **API base URL:** `https://api.opensea.io`

## Authentication

### API Key

Authenticate OpenSea API requests with an OpenSea developer API key sent in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.opensea.io/reference/api-keys)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (50 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Build Mint Transaction Data For Drop](actions/build-drop-mint-transaction.md) | `POST /api/v2/drops/{slug}/mint` | [docs](https://docs.opensea.io/reference/build_drop_mint_transaction) |
| [Build Criteria Offer](actions/build-offer-v2.md) | `POST /api/v2/offers/build` | [docs](https://docs.opensea.io/reference/build_offer_v2) |
| [Cancel Order](actions/cancel-order.md) | `POST /api/v2/orders/chain/{chain}/protocol/{protocol_address}/{order_hash}/cancel` | [docs](https://docs.opensea.io/reference/cancel_order) |
| [Fulfill Listing](actions/generate-listing-fulfillment-data-v2.md) | `POST /api/v2/listings/fulfillment_data` | [docs](https://docs.opensea.io/reference/generate_listing_fulfillment_data_v2) |
| [Fulfill Offer](actions/generate-offer-fulfillment-data-v2.md) | `POST /api/v2/offers/fulfillment_data` | [docs](https://docs.opensea.io/reference/generate_offer_fulfillment_data_v2) |
| [Get OpenSea Account Profile](actions/get-account.md) | `GET /api/v2/accounts/{address_or_username}` | [docs](https://docs.opensea.io/reference/get_account) |
| [Get Best Listing By NFT](actions/get-best-listing-nft.md) | `GET /api/v2/listings/collection/{slug}/nfts/{identifier}/best` | [docs](https://docs.opensea.io/reference/get_best_listing_nft) |
| [Get Best Listings By Collection](actions/get-best-listings-collection.md) | `GET /api/v2/listings/collection/{slug}/best` | [docs](https://docs.opensea.io/reference/get_best_listings_collection) |
| [Get Best Offer By NFT](actions/get-best-offer-nft.md) | `GET /api/v2/offers/collection/{slug}/nfts/{identifier}/best` | [docs](https://docs.opensea.io/reference/get_best_offer_nft) |
| [Get Supported Chains Catalog](actions/get-chains.md) | `GET /api/v2/chains` | [docs](https://docs.opensea.io/reference/get_chains) |
| [Get Single Collection](actions/get-collection.md) | `GET /api/v2/collections/{slug}` | [docs](https://docs.opensea.io/reference/get_collection) |
| [Get Collection Stats](actions/get-collection-stats.md) | `GET /api/v2/collections/{slug}/stats` | [docs](https://docs.opensea.io/reference/get_collection_stats) |
| [Get Collection Traits](actions/get-collection-traits.md) | `GET /api/v2/traits/{slug}` | [docs](https://docs.opensea.io/reference/get_collection_traits) |
| [Get Contract](actions/get-contract.md) | `GET /api/v2/chain/{chain}/contract/{address}` | [docs](https://docs.opensea.io/reference/get_contract) |
| [Get Drop By Collection Slug](actions/get-drop-by-slug.md) | `GET /api/v2/drops/{slug}` | [docs](https://docs.opensea.io/reference/get_drop_by_slug) |
| [Get Drops](actions/get-drops.md) | `GET /api/v2/drops` | [docs](https://docs.opensea.io/reference/get_drops) |
| [Get Listings](actions/get-listings.md) | `GET /api/v2/orders/{chain}/{protocol}/listings` | [docs](https://docs.opensea.io/reference/get_listings) |
| [Get NFT](actions/get-nft.md) | `GET /api/v2/chain/{chain}/contract/{address}/nfts/{identifier}` | [docs](https://docs.opensea.io/reference/get_nft) |
| [Get Collection By NFT](actions/get-nft-collection.md) | `GET /api/v2/chain/{chain}/contract/{address}/nfts/{identifier}/collection` | [docs](https://docs.opensea.io/reference/get_nft_collection) |
| [Get NFT Metadata](actions/get-nft-metadata.md) | `GET /api/v2/metadata/{chain}/{contractAddress}/{tokenId}` | [docs](https://docs.opensea.io/reference/get_nft_metadata) |
| [Get NFTs By Account](actions/get-nfts-by-account.md) | `GET /api/v2/chain/{chain}/account/{address}/nfts` | [docs](https://docs.opensea.io/reference/get_nfts_by_account) |
| [Get NFTs By Collection](actions/get-nfts-by-collection.md) | `GET /api/v2/collection/{slug}/nfts` | [docs](https://docs.opensea.io/reference/get_nfts_by_collection) |
| [Get NFTs By Contract](actions/get-nfts-by-contract.md) | `GET /api/v2/chain/{chain}/contract/{address}/nfts` | [docs](https://docs.opensea.io/reference/get_nfts_by_contract) |
| [Get Item Offers](actions/get-offers.md) | `GET /api/v2/orders/{chain}/{protocol}/offers` | [docs](https://docs.opensea.io/reference/get_offers) |
| [Get Offers By Collection](actions/get-offers-collection.md) | `GET /api/v2/offers/collection/{slug}` | [docs](https://docs.opensea.io/reference/get_offers_collection) |
| [Get Offers By Trait](actions/get-offers-collection-trait.md) | `GET /api/v2/offers/collection/{slug}/traits` | [docs](https://docs.opensea.io/reference/get_offers_collection_trait) |
| [Get Offers By NFT](actions/get-offers-nft.md) | `GET /api/v2/offers/collection/{slug}/nfts/{identifier}` | [docs](https://docs.opensea.io/reference/get_offers_nft) |
| [Get Order](actions/get-order.md) | `GET /api/v2/orders/chain/{chain}/protocol/{protocol_address}/{order_hash}` | [docs](https://docs.opensea.io/reference/get_order) |
| [Get Payment Token Details](actions/get-payment-token.md) | `GET /api/v2/chain/{chain}/payment_token/{address}` | [docs](https://docs.opensea.io/reference/get_payment_token) |
| [Get Swap Quote](actions/get-swap-quote.md) | `GET /api/v2/swap/quote` | [docs](https://docs.opensea.io/reference/get_swap_quote) |
| [Get Token Details Catalog](actions/get-token.md) | `GET /api/v2/chain/{chain}/token/{address}` | [docs](https://docs.opensea.io/reference/get_token) |
| [Get Token Balances By Wallet](actions/get-token-balances-by-account.md) | `GET /api/v2/account/{address}/tokens` | [docs](https://docs.opensea.io/reference/get_token_balances_by_account) |
| [Get Top Collections](actions/get-top-collections.md) | `GET /api/v2/collections/top` | [docs](https://docs.opensea.io/reference/get_top_collections) |
| [Get Top Tokens](actions/get-top-tokens.md) | `GET /api/v2/tokens/top` | [docs](https://docs.opensea.io/reference/get_top_tokens) |
| [Get Trending Collections](actions/get-trending-collections.md) | `GET /api/v2/collections/trending` | [docs](https://docs.opensea.io/reference/get_trending_collections) |
| [Get Trending Tokens](actions/get-trending-tokens.md) | `GET /api/v2/tokens/trending` | [docs](https://docs.opensea.io/reference/get_trending_tokens) |
| [Get Multiple Collections](actions/list-collections.md) | `GET /api/v2/collections` | [docs](https://docs.opensea.io/reference/list_collections) |
| [Get Events](actions/list-events.md) | `GET /api/v2/events` | [docs](https://docs.opensea.io/reference/list_events) |
| [Get Events By Account](actions/list-events-by-account.md) | `GET /api/v2/events/accounts/{address}` | [docs](https://docs.opensea.io/reference/list_events_by_account) |
| [Get Events By Collection](actions/list-events-by-collection.md) | `GET /api/v2/events/collection/{slug}` | [docs](https://docs.opensea.io/reference/list_events_by_collection) |
| [Get Events By NFT](actions/list-events-by-nft.md) | `GET /api/v2/events/chain/{chain}/contract/{address}/nfts/{identifier}` | [docs](https://docs.opensea.io/reference/list_events_by_nft) |
| [Get All Listings By Collection](actions/list-listings-collection-all.md) | `GET /api/v2/listings/collection/{slug}/all` | [docs](https://docs.opensea.io/reference/list_listings_collection_all) |
| [Get All Offers By Collection](actions/list-offers-collection-all.md) | `GET /api/v2/offers/collection/{slug}/all` | [docs](https://docs.opensea.io/reference/list_offers_collection_all) |
| [Create Criteria Offer](actions/post-criteria-offer-v2.md) | `POST /api/v2/offers` | [docs](https://docs.opensea.io/reference/post_criteria_offer_v2) |
| [Create Listing](actions/post-listing.md) | `POST /api/v2/orders/{chain}/{protocol}/listings` | [docs](https://docs.opensea.io/reference/post_listing) |
| [Create Item Offer](actions/post-offer.md) | `POST /api/v2/orders/{chain}/{protocol}/offers` | [docs](https://docs.opensea.io/reference/post_offer) |
| [Refresh NFT Metadata](actions/refresh-nft-metadata.md) | `POST /api/v2/chain/{chain}/contract/{address}/nfts/{identifier}/refresh` | [docs](https://docs.opensea.io/reference/refresh_nft_metadata) |
| [Resolve Account Identifier](actions/resolve-account.md) | `GET /api/v2/accounts/resolve/{identifier}` | [docs](https://docs.opensea.io/reference/resolve_account) |
| [Search OpenSea](actions/search.md) | `GET /api/v2/search` | [docs](https://docs.opensea.io/reference/search) |
| [Validate NFT Metadata](actions/validate-nft-metadata.md) | `POST /api/v2/chain/{chain}/contract/{address}/nfts/{identifier}/validate-metadata` | [docs](https://docs.opensea.io/reference/validate_nft_metadata) |
