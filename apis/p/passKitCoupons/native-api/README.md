# PassKit Coupons: Native API Reference

A consolidated summary of PassKit Coupons's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://docs.passkit.io/
- **OpenAPI specification:** https://docs.passkit.io/protocols/coupon/coupon.swagger.json
- **API base URL:** `https://api.pub2.passkit.io`

## Authentication

### JWT

Generate a signed PassKit JWT from your REST API key and secret for each API request.

### Credentials

- **API Key:** `apiKey` · required · PassKit REST API key from Developer Tools > REST Credentials.
- **API Secret:** `apiSecret` · required · PassKit REST API secret from Developer Tools > REST Credentials.

[Official authentication documentation](https://help.passkit.com/en/articles/4138220-2-steps-to-call-passkit-api-from-google-app-script)

## Pagination

Use `limit` in the request body to set the page size (default 25; minimum -1). Use `offset` in the request body as the record offset; numbering starts at 0.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Void Coupons](actions/bulk-void-coupons.md) | `DELETE /coupon/singleUse/coupons/bulk` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Copy Campaign](actions/copy-campaign.md) | `POST /coupon/singleUse/campaign/copy` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Count Coupons](actions/count-coupons.md) | `POST /coupon/singleUse/coupons/count/:couponCampaignId` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Create Coupon](actions/create-coupon.md) | `POST /coupon/singleUse/coupon` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Create Coupon Campaign](actions/create-coupon-campaign.md) | `POST /coupon/singleUse/campaign` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Create Coupon Offer](actions/create-coupon-offer.md) | `POST /coupon/singleUse/offer` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Delete Coupon Campaign](actions/delete-coupon-campaign.md) | `DELETE /coupon/singleUse/campaign/:id` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Delete Coupon Offer](actions/delete-coupon-offer.md) | `DELETE /coupon/singleUse/offer/:id` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Get Coupon by External ID](actions/get-coupon-by-external-id.md) | `GET /coupon/singleUse/coupon/externalId/:couponCampaignId/:externalId` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Get Coupon by ID](actions/get-coupon-by-id.md) | `GET /coupon/singleUse/coupon/:id` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Get Coupon Campaign](actions/get-coupon-campaign.md) | `GET /coupon/singleUse/campaign/:id` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Get Coupon Campaign Analytics](actions/get-coupon-campaign-analytics.md) | `GET /coupon/singleUse/campaign/:classId/analytics` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Get Coupon Offer](actions/get-coupon-offer.md) | `GET /coupon/singleUse/offer/:id` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Get Meta Keys for a Campaign](actions/get-meta-keys-for-a-campaign.md) | `GET /coupon/singleUse/campaign/meta/:id` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Get User Profile](actions/get-user-profile.md) | `GET /user/profile` | [docs](https://docs.passkit.io/) |
| [List Coupon Campaigns](actions/list-coupon-campaigns.md) | `POST /coupon/singleUse/campaigns/list` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [List Coupon Offers](actions/list-coupon-offers.md) | `POST /coupon/singleUse/offers/list` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [List Coupons](actions/list-coupons.md) | `POST /coupon/singleUse/coupons/list/:couponCampaignId` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Redeem Coupon](actions/redeem-coupon.md) | `PUT /coupon/singleUse/coupon/redeem` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Update Coupon](actions/update-coupon.md) | `PUT /coupon/singleUse/coupon` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Update Coupon Campaign](actions/update-coupon-campaign.md) | `PUT /coupon/singleUse/campaign` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Update Coupon External Id](actions/update-coupon-external-id.md) | `PUT /coupon/singleUse/coupon/externalId` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Update Coupon Offer](actions/update-coupon-offer.md) | `PUT /coupon/singleUse/offer` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Update Personal Information](actions/update-personal-information.md) | `PATCH /coupon/singleUse/coupon/person` | [docs](https://docs.passkit.io/protocols/coupon/) |
| [Void Coupon](actions/void-coupon.md) | `DELETE /coupon/singleUse/coupon` | [docs](https://docs.passkit.io/protocols/coupon/) |
