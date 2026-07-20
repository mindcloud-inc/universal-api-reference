# <img src="https://images.mindcloud.co/apps/icons/pass-kit-coupons_1774547524417.png" alt="PassKit Coupons logo" width="28" height="28"> PassKit Coupons: Universal API

PassKit Coupons lets teams create and manage PassKit single-use coupon campaigns, offers, coupons, and coupon analytics through PassKit's coupon APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/passKitCoupons/latest
- **Category:** Marketing
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://passkit.com/
- **Vendor API docs:** https://docs.passkit.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Profile](actions/get-user-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Coupon

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Void Coupons](actions/bulk-void-coupons.md) | DELETE |  |
| [Create Coupon](actions/create-coupon.md) | POST |  |
| [Get Coupon by External ID](actions/get-coupon-by-external-id.md) | GET |  |
| [Get Coupon by ID](actions/get-coupon-by-id.md) | GET |  |
| [List Coupons](actions/list-coupons.md) | GET |  |
| [Redeem Coupon](actions/redeem-coupon.md) | PUT |  |
| [Update Coupon](actions/update-coupon.md) | PUT |  |
| [Update Coupon External Id](actions/update-coupon-external-id.md) | PUT |  |
| [Update Personal Information](actions/update-personal-information.md) | PUT |  |
| [Void Coupon](actions/void-coupon.md) | DELETE |  |

### Coupon Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Copy Campaign](actions/copy-campaign.md) | POST |  |
| [Create Coupon Campaign](actions/create-coupon-campaign.md) | POST |  |
| [Delete Coupon Campaign](actions/delete-coupon-campaign.md) | DELETE |  |
| [Get Coupon Campaign](actions/get-coupon-campaign.md) | GET |  |
| [List Coupon Campaigns](actions/list-coupon-campaigns.md) | GET |  |
| [Update Coupon Campaign](actions/update-coupon-campaign.md) | PUT |  |

### Coupon Campaign Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Coupon Campaign Analytics](actions/get-coupon-campaign-analytics.md) | GET |  |

### Coupon Campaign Meta Key

| Action | Method | Description |
| --- | --- | --- |
| [Get Meta Keys for a Campaign](actions/get-meta-keys-for-a-campaign.md) | GET |  |

### Coupon Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Coupons](actions/count-coupons.md) | GET |  |

### Coupon Offer

| Action | Method | Description |
| --- | --- | --- |
| [Create Coupon Offer](actions/create-coupon-offer.md) | POST |  |
| [Delete Coupon Offer](actions/delete-coupon-offer.md) | DELETE |  |
| [Get Coupon Offer](actions/get-coupon-offer.md) | GET |  |
| [List Coupon Offers](actions/list-coupon-offers.md) | GET |  |
| [Update Coupon Offer](actions/update-coupon-offer.md) | PUT |  |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET |  |

