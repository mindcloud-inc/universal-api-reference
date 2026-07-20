# <img src="https://images.mindcloud.co/apps/icons/rakuten-advertising-icon_1776797472400.png" alt="Rakuten Advertising logo" width="28" height="28"> Rakuten Advertising: Universal API

Get your API access token in Rakuten by opening Applications, clicking Generate Token, entering your numerical publisher SID in Token Scope (sid), and copying the generated bearer token here. Do not use APIs > Manage Tokens.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rakutenAdvertising/latest
- **Category:** Marketing
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rakutenadvertising.com/
- **Vendor API docs:** https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List advertisers](actions/list-advertisers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/list-advertisers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Advanced Report Row

| Action | Method | Description |
| --- | --- | --- |
| [Run advanced report](actions/run-advanced-report.md) | GET | Retrieves an advanced report from Rakuten Advertising. |
| [Run advertiser advanced report](actions/run-advertiser-advanced-report.md) | GET | Retrieves an advertiser advanced report from Rakuten Advertising. |
| [Run localized advanced report](actions/run-localized-advanced-report.md) | GET | Retrieves a localized advanced report from Rakuten Advertising. |
| [Run network advanced report](actions/run-network-advanced-report.md) | GET | Retrieves a network advanced report from Rakuten Advertising. |

### Advertiser

| Action | Method | Description |
| --- | --- | --- |
| [Get advertiser](actions/get-advertiser.md) | GET | Retrieves an advertiser from Rakuten Advertising. |
| [List advertisers](actions/list-advertisers.md) | GET | Retrieves advertisers from Rakuten Advertising. |

### Advertiser Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search advertisers](actions/search-advertisers.md) | GET | Finds advertisers in Rakuten Advertising by search criteria. |

### Banner Link

| Action | Method | Description |
| --- | --- | --- |
| [Get banner links](actions/get-banner-links.md) | GET | Retrieves banner links from Rakuten Advertising. |

### Commissioning List

| Action | Method | Description |
| --- | --- | --- |
| [Get commissioning list](actions/get-commissioning-list.md) | GET | Retrieves a commissioning list from Rakuten Advertising. |
| [List commissioning lists](actions/list-commissioning-lists.md) | GET | Retrieves commissioning lists from Rakuten Advertising. |

### Contributed Conversion

| Action | Method | Description |
| --- | --- | --- |
| [List contributed conversions](actions/list-contributed-conversions.md) | GET | Retrieves contributed conversions from Rakuten Advertising. |

### Coupon

| Action | Method | Description |
| --- | --- | --- |
| [List coupons](actions/list-coupons.md) | GET | Retrieves coupons from Rakuten Advertising. |

### Coupon Metadata

| Action | Method | Description |
| --- | --- | --- |
| [List coupon metadata](actions/list-coupon-metadata.md) | GET | Retrieves coupon metadata from Rakuten Advertising. |

### Creative Category

| Action | Method | Description |
| --- | --- | --- |
| [Get creative categories](actions/get-creative-categories.md) | GET | Retrieves creative categories from Rakuten Advertising. |

### Deep Link

| Action | Method | Description |
| --- | --- | --- |
| [Create deep link](actions/create-deep-link.md) | POST | Creates a deep link in Rakuten Advertising. |

### Drm Link

| Action | Method | Description |
| --- | --- | --- |
| [Get DRM links](actions/get-drm-links.md) | GET | Retrieves DRM links from Rakuten Advertising. |

### Invoice Item Report Row

| Action | Method | Description |
| --- | --- | --- |
| [Get invoice item report](actions/get-invoice-item-report.md) | GET | Retrieves an invoice item report from Rakuten Advertising. |

### Invoice Report Row

| Action | Method | Description |
| --- | --- | --- |
| [Get invoice report](actions/get-invoice-report.md) | GET | Retrieves an invoice report from Rakuten Advertising. |

### Merchant

| Action | Method | Description |
| --- | --- | --- |
| [Get merchant by ID](actions/get-merchant-by-id.md) | GET | Retrieves a merchant from Rakuten Advertising by advertiser ID. |
| [Get merchants by application status](actions/get-merchants-by-application-status.md) | GET | Retrieves merchants from Rakuten Advertising by application status. |
| [Get merchants by category](actions/get-merchants-by-category.md) | GET | Retrieves merchants from Rakuten Advertising by category. |
| [Get merchants by name](actions/get-merchants-by-name.md) | GET | Finds merchants in Rakuten Advertising by name. |

### Offer

| Action | Method | Description |
| --- | --- | --- |
| [Get offer](actions/get-offer.md) | GET | Retrieves an offer from Rakuten Advertising. |
| [List offers](actions/list-offers.md) | GET | Retrieves offers from Rakuten Advertising. |

### Partnership

| Action | Method | Description |
| --- | --- | --- |
| [Get partnership](actions/get-partnership.md) | GET | Retrieves a partnership from Rakuten Advertising. |
| [List partnerships](actions/list-partnerships.md) | GET | Retrieves partnerships from Rakuten Advertising. |

### Payment Report Row

| Action | Method | Description |
| --- | --- | --- |
| [Get payment report](actions/get-payment-report.md) | GET | Retrieves a payment report from Rakuten Advertising. |

### Postback

| Action | Method | Description |
| --- | --- | --- |
| [Create postback](actions/create-postback.md) | POST | Creates a new postback in Rakuten Advertising. |
| [Delete postback](actions/delete-postback.md) | DELETE | Deletes an existing postback from Rakuten Advertising. |
| [Get postback](actions/get-postback.md) | GET | Retrieves a postback from Rakuten Advertising. |
| [Update postback](actions/update-postback.md) | PUT | Updates an existing postback in Rakuten Advertising. |

### Product Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search products](actions/search-products.md) | GET | Finds products in Rakuten Advertising by search criteria. |

### Signature Orders Payment Report Row

| Action | Method | Description |
| --- | --- | --- |
| [Get signature orders payment report](actions/get-signature-orders-payment-report.md) | GET | Retrieves a signature orders payment report from Rakuten Advertising. |

### Text Link

| Action | Method | Description |
| --- | --- | --- |
| [Get text links](actions/get-text-links.md) | GET | Retrieves text links from Rakuten Advertising. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List transactions](actions/list-transactions.md) | GET | Retrieves transactions from Rakuten Advertising. |

