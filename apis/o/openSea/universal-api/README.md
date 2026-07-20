# <img src="https://images.mindcloud.co/apps/icons/open-sea-icon-square_1776188318686.png" alt="OpenSea logo" width="28" height="28"> OpenSea: Universal API

OpenSea marketplace API for collections, NFTs, events, orders, listings, offers, drops, search, and token data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openSea/latest
- **Category:** Commerce
- **Actions:** 50
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://opensea.io
- **Vendor API docs:** https://docs.opensea.io/reference/api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Supported Chains Catalog](actions/get-chains.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-chains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (50)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get OpenSea Account Profile](actions/get-account.md) | GET | Retrieves an OpenSea account profile. |
| [Resolve Account Identifier](actions/resolve-account.md) | GET | Resolves an OpenSea account identifier. |

### Chain

| Action | Method | Description |
| --- | --- | --- |
| [Get Supported Chains Catalog](actions/get-chains.md) | GET | Retrieves supported chains from OpenSea. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Get Single Collection](actions/get-collection.md) | GET | Retrieves a collection from OpenSea. |
| [Get Collection Stats](actions/get-collection-stats.md) | GET | Retrieves collection stats from OpenSea. |
| [Get Collection By NFT](actions/get-nft-collection.md) | GET | Retrieves an NFT's collection from OpenSea. |
| [Get Top Collections](actions/get-top-collections.md) | GET | Retrieves top collections from OpenSea. |
| [Get Trending Collections](actions/get-trending-collections.md) | GET | Retrieves trending collections from OpenSea. |
| [Get Multiple Collections](actions/list-collections.md) | GET | Retrieves collections from OpenSea. |

### Contract

| Action | Method | Description |
| --- | --- | --- |
| [Get Contract](actions/get-contract.md) | GET | Retrieves a contract from OpenSea. |

### Drop

| Action | Method | Description |
| --- | --- | --- |
| [Get Drop By Collection Slug](actions/get-drop-by-slug.md) | GET | Retrieves a drop from OpenSea. |
| [Get Drops](actions/get-drops.md) | GET | Retrieves drops from OpenSea. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Events](actions/list-events.md) | GET | Retrieves events from OpenSea. |
| [Get Events By Account](actions/list-events-by-account.md) | GET | Retrieves events for an OpenSea account. |
| [Get Events By Collection](actions/list-events-by-collection.md) | GET | Retrieves events for an OpenSea collection. |
| [Get Events By NFT](actions/list-events-by-nft.md) | GET | Retrieves events for an NFT in OpenSea. |

### Listing

| Action | Method | Description |
| --- | --- | --- |
| [Get Best Listing By NFT](actions/get-best-listing-nft.md) | GET | Retrieves the best listing for an NFT in OpenSea. |
| [Get Best Listings By Collection](actions/get-best-listings-collection.md) | GET | Retrieves best listings for an OpenSea collection. |
| [Get Listings](actions/get-listings.md) | GET |  |
| [Get All Listings By Collection](actions/list-listings-collection-all.md) | GET | Retrieves all listings for an OpenSea collection. |
| [Create Listing](actions/post-listing.md) | POST | Creates a listing in OpenSea. |

### Listing Fulfillment

| Action | Method | Description |
| --- | --- | --- |
| [Fulfill Listing](actions/generate-listing-fulfillment-data-v2.md) | GET | Retrieves listing fulfillment data from OpenSea. |

### Mint Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Build Mint Transaction Data For Drop](actions/build-drop-mint-transaction.md) | GET | Builds mint transaction data for an OpenSea drop. |

### Nft

| Action | Method | Description |
| --- | --- | --- |
| [Get NFT](actions/get-nft.md) | GET | Retrieves an NFT from OpenSea. |
| [Get NFT Metadata](actions/get-nft-metadata.md) | GET | Retrieves NFT metadata from OpenSea. |
| [Get NFTs By Account](actions/get-nfts-by-account.md) | GET | Retrieves NFTs owned by an OpenSea account. |
| [Get NFTs By Collection](actions/get-nfts-by-collection.md) | GET | Retrieves NFTs in an OpenSea collection. |
| [Get NFTs By Contract](actions/get-nfts-by-contract.md) | GET | Retrieves NFTs for a contract in OpenSea. |
| [Refresh NFT Metadata](actions/refresh-nft-metadata.md) | PUT | Refreshes NFT metadata in OpenSea. |
| [Validate NFT Metadata](actions/validate-nft-metadata.md) | PUT | Validates NFT metadata in OpenSea. |

### Offer

| Action | Method | Description |
| --- | --- | --- |
| [Get Best Offer By NFT](actions/get-best-offer-nft.md) | GET | Retrieves the best offer for an NFT in OpenSea. |
| [Get Item Offers](actions/get-offers.md) | GET |  |
| [Get Offers By Collection](actions/get-offers-collection.md) | GET | Retrieves offers for an OpenSea collection. |
| [Get Offers By Trait](actions/get-offers-collection-trait.md) | GET | Retrieves offers for a trait in OpenSea. |
| [Get Offers By NFT](actions/get-offers-nft.md) | GET | Retrieves offers for an NFT in OpenSea. |
| [Get All Offers By Collection](actions/list-offers-collection-all.md) | GET | Retrieves all offers for an OpenSea collection. |
| [Create Criteria Offer](actions/post-criteria-offer-v2.md) | POST | Creates a criteria offer in OpenSea. |
| [Create Item Offer](actions/post-offer.md) | POST | Creates an item offer in OpenSea. |

### Offer Build

| Action | Method | Description |
| --- | --- | --- |
| [Build Criteria Offer](actions/build-offer-v2.md) | GET | Builds a criteria offer in OpenSea. |

### Offer Fulfillment

| Action | Method | Description |
| --- | --- | --- |
| [Fulfill Offer](actions/generate-offer-fulfillment-data-v2.md) | GET | Retrieves offer fulfillment data from OpenSea. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Order](actions/cancel-order.md) | DELETE | Cancels an order in OpenSea. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from OpenSea. |

### Payment Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Payment Token Details](actions/get-payment-token.md) | GET | Retrieves a payment token from OpenSea. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search OpenSea](actions/search.md) | GET | Finds items in OpenSea by search term. |

### Swap Quote

| Action | Method | Description |
| --- | --- | --- |
| [Get Swap Quote](actions/get-swap-quote.md) | GET | Retrieves a swap quote from OpenSea. |

### Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Token Details Catalog](actions/get-token.md) | GET | Retrieves a token from OpenSea. |
| [Get Top Tokens](actions/get-top-tokens.md) | GET | Retrieves top tokens from OpenSea. |
| [Get Trending Tokens](actions/get-trending-tokens.md) | GET | Retrieves trending tokens from OpenSea. |

### Token Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Token Balances By Wallet](actions/get-token-balances-by-account.md) | GET | Retrieves token balances for an OpenSea account. |

### Trait

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection Traits](actions/get-collection-traits.md) | GET | Retrieves collection traits from OpenSea. |

