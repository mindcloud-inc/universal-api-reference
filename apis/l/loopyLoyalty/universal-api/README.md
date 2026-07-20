# <img src="https://images.mindcloud.co/apps/icons/id-xwa80gg-n-1774386010681_1774386015826.jpeg" alt="Loopy Loyalty logo" width="28" height="28"> Loopy Loyalty: Universal API

Create loyalty cards, message customers, and track program performance

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/loopyLoyalty/latest
- **Category:** Marketing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://loopyloyalty.com
- **Vendor API docs:** https://developer.loopyloyalty.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Stamp Images](actions/list-stamp-images.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-stamp-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Beacon

| Action | Method | Description |
| --- | --- | --- |
| [List Beacons](actions/list-beacons.md) | GET |  |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Campaign Exists By Name](actions/campaign-exists-by-name.md) | GET |  |
| [Create Campaign](actions/create-campaign.md) | POST |  |
| [Get Campaign By ID](actions/get-campaign-by-id.md) | GET |  |
| [Get Campaign By Name](actions/get-campaign-by-name.md) | GET |  |
| [Get Campaign Public](actions/get-campaign-public.md) | GET |  |
| [List Campaigns](actions/list-campaigns.md) | GET |  |
| [Push Latest Campaign Changes](actions/push-latest-campaign-changes.md) | PUT |  |
| [Update Campaign](actions/update-campaign.md) | PUT |  |

### Campaign Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Campaign](actions/export-campaign.md) | POST |  |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Delete Campaign](actions/delete-campaign.md) | DELETE |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Add Stamps By Card ID](actions/add-stamps-by-card-id.md) | PUT |  |
| [Enrol Customer](actions/enrol-customer.md) | POST |  |
| [Get Card By ID](actions/get-card-by-id.md) | GET |  |
| [Get Card By Unique ID](actions/get-card-by-unique-id.md) | GET |  |
| [List Cards](actions/list-cards.md) | GET |  |
| [Redeem Rewards By Card ID](actions/redeem-rewards-by-card-id.md) | PUT |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Add Stamps By Unique Card Data Field](actions/add-stamps-by-unique-card-data-field.md) | PUT |  |
| [Delete Card By ID](actions/delete-card-by-id.md) | DELETE |  |
| [Re-Sync Card](actions/re-sync-card.md) | PUT |  |
| [Redeem Rewards By Unique Card Data Field](actions/redeem-rewards-by-unique-card-data-field.md) | PUT |  |
| [Send Message To All Cards](actions/send-message-to-all-cards.md) | PUT |  |
| [Send Message To An Individual Card](actions/send-message-to-an-individual-card.md) | PUT |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events For Campaign](actions/list-events-for-campaign.md) | GET |  |

### Image Asset

| Action | Method | Description |
| --- | --- | --- |
| [Create Image Asset](actions/create-image-asset.md) | POST |  |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST |  |
| [Delete Location](actions/delete-location.md) | DELETE |  |
| [Get Location](actions/get-location.md) | GET |  |
| [List Locations](actions/list-locations.md) | GET |  |
| [Update Location](actions/update-location.md) | PUT |  |

### Stamp Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Stamp Image By ID](actions/get-stamp-image-by-id.md) | GET |  |

### Stamp Template

| Action | Method | Description |
| --- | --- | --- |
| [List Stamp Images](actions/list-stamp-images.md) | GET |  |

### Strip Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Strip Image By Image Configuration](actions/get-strip-image-by-image-configuration.md) | GET |  |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST |  |
| [Delete Subscription](actions/delete-subscription.md) | DELETE |  |

### Subuser

| Action | Method | Description |
| --- | --- | --- |
| [Create Subuser](actions/create-subuser.md) | POST |  |
| [Delete Subuser](actions/delete-subuser.md) | DELETE |  |
| [Get Subuser](actions/get-subuser.md) | GET |  |
| [List Subusers](actions/list-subusers.md) | GET |  |
| [Update Subuser](actions/update-subuser.md) | PUT |  |

