# Loopy Loyalty: Native API Reference

A consolidated summary of Loopy Loyalty's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.loopyloyalty.com/
- **OpenAPI specification:** https://developer.loopyloyalty.com/loopyloyalty.swagger.json
- **API base URL:** `https://api.loopyloyalty.com/v1`

## Authentication

### Signed JWT

Sign a JWT with your Loopy Loyalty API secret and send it in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required · Your Loopy Loyalty API key. The signed JWT uses this value as the uid claim.
- **Username:** `username` · required · The Loopy Loyalty account or subuser username included in the JWT username claim.

[Official authentication documentation](https://developer.loopyloyalty.com/loopyloyalty.swagger.json)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Stamps By Card ID](actions/add-stamps-by-card-id.md) | `POST /card/cid/:cid/addStamps/:stamps` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_addStamps) |
| [Add Stamps By Unique Card Data Field](actions/add-stamps-by-unique-card-data-field.md) | `POST /uniquecard/campaignid/:campaignId/:uniqueIdType/:uniqueIdValue/addStamps/:stamps` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_addStampsByUniqueCardField) |
| [Campaign Exists By Name](actions/campaign-exists-by-name.md) | `GET /campaign/exists/:name` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_campaignExists) |
| [Create Campaign](actions/create-campaign.md) | `POST /campaign` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_createCampaign) |
| [Create Image Asset](actions/create-image-asset.md) | `POST /imageAsset` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_createImageAssets) |
| [Create Location](actions/create-location.md) | `POST /location` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_createLocation) |
| [Create Subscription](actions/create-subscription.md) | `POST /subscription` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_createSubscription) |
| [Create Subuser](actions/create-subuser.md) | `POST /subuser` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_createSubuser) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE /campaign/:id` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_deleteCampaign) |
| [Delete Card By ID](actions/delete-card-by-id.md) | `DELETE /card/cid/:id/delete` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_deleteCard) |
| [Delete Location](actions/delete-location.md) | `DELETE /location/:id` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_deleteLocation) |
| [Delete Subscription](actions/delete-subscription.md) | `DELETE /subscription/:id` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_deleteSubscription) |
| [Delete Subuser](actions/delete-subuser.md) | `DELETE /subuser/:id` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_deleteSubuser) |
| [Enrol Customer](actions/enrol-customer.md) | `POST /enrol/:campaignId` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_enrolMember) |
| [Export Campaign](actions/export-campaign.md) | `POST /export/:id` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_exportCampaign) |
| [Get Campaign By ID](actions/get-campaign-by-id.md) | `GET /campaign/id/:id` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_getCampaignById) |
| [Get Campaign By Name](actions/get-campaign-by-name.md) | `GET /campaign/name/:name` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_getCampaignByName) |
| [Get Campaign Public](actions/get-campaign-public.md) | `GET /campaign/public/:id` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_getCampaignPublic) |
| [Get Card By ID](actions/get-card-by-id.md) | `GET /card/:cid` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_getCardById) |
| [Get Card By Unique ID](actions/get-card-by-unique-id.md) | `GET /uniquecard/campaignid/:campaignId/:uniqueIdType/:uniqueIdValue` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_getCardByUniqueId) |
| [Get Location](actions/get-location.md) | `GET /location/:id` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_getLocation) |
| [Get Stamp Image By ID](actions/get-stamp-image-by-id.md) | `GET /images/stampImage/:id` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_getStampImage) |
| [Get Strip Image By Image Configuration](actions/get-strip-image-by-image-configuration.md) | `GET /images` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_getStripImage) |
| [Get Subuser](actions/get-subuser.md) | `GET /subuser/:id` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_getSubuser) |
| [List Beacons](actions/list-beacons.md) | `GET /beacons` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_listBeacons) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_listCampaigns) |
| [List Cards](actions/list-cards.md) | `POST /card/cid/:cid` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_listCards) |
| [List Events For Campaign](actions/list-events-for-campaign.md) | `POST /events/analytics/transactions/:cid` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_listEventsForCampaign) |
| [List Locations](actions/list-locations.md) | `GET /locations` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_listLocations) |
| [List Stamp Images](actions/list-stamp-images.md) | `GET /images/stampTemplates` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_listStampImages) |
| [List Subusers](actions/list-subusers.md) | `GET /subusers` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_listSubUsers) |
| [Push Latest Campaign Changes](actions/push-latest-campaign-changes.md) | `POST /campaign/:id/push` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_pushChangesToCards) |
| [Re-Sync Card](actions/re-sync-card.md) | `PUT /card/cid/:cid/resync` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_resyncCard) |
| [Redeem Rewards By Card ID](actions/redeem-rewards-by-card-id.md) | `POST /card/cid/:cid/redeemReward/:rewardType/:rewardsToRedeem` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_redeemReward) |
| [Redeem Rewards By Unique Card Data Field](actions/redeem-rewards-by-unique-card-data-field.md) | `POST /uniquecard/campaignid/:campaignId/:uniqueIdType/:uniqueIdValue/redeemReward/:rewardType/:rewardsToRedeem` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_redeemRewardByUniqueCardField) |
| [Send Message To All Cards](actions/send-message-to-all-cards.md) | `POST /card/cid/:cid/push` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_sendMessageToAllCards) |
| [Send Message To An Individual Card](actions/send-message-to-an-individual-card.md) | `POST /card/push` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_sendMessageToIndividualCard) |
| [Update Campaign](actions/update-campaign.md) | `PATCH /campaign/:id` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_updateCampaign) |
| [Update Location](actions/update-location.md) | `PATCH /location/:id` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_updateLocation) |
| [Update Subuser](actions/update-subuser.md) | `PATCH /subuser/:id` | [docs](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_updateSubuser) |
