# <img src="https://images.mindcloud.co/apps/icons/absinthe_1774992049099.png" alt="Absinthe logo" width="28" height="28"> Absinthe: Universal API

The definitive API for community-powered gamification via campaigns, badges, points, inventory, and redemptions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/absinthe/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.absinthe.network/
- **Vendor API docs:** https://api.absinthe.network/doc

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Campaigns](actions/list-campaigns.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/absinthe/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [List Point Sources](actions/list-point-sources.md) | GET | Retrieves point sources from an Absinthe campaign. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns for your Absinthe organization. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Registered Event](actions/create-registered-event.md) | POST | Creates a registered event in an Absinthe campaign. |
| [List Registered Events](actions/list-registered-events.md) | GET | Retrieves registered events from an Absinthe campaign. |
| [Submit Event Data](actions/submit-event-data.md) | POST | Submits event data to an Absinthe registered event. |

### Fulfillments

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Redemptions](actions/get-campaign-redemptions.md) | GET | Retrieves campaign redemptions and fulfillment status from Absinthe. |
| [Get User Redemptions](actions/get-user-redemptions.md) | GET | Retrieves a user's redemption history from Absinthe. |
| [Redeem an Item](actions/redeem-an-item.md) | POST | Redeems a reward item for a user in Absinthe. |
| [Refund a Redemption](actions/refund-a-redemption.md) | POST | Refunds a redemption for a user in Absinthe. |
| [Update Redemption Status](actions/update-redemption-status.md) | PUT | Updates a redemption's status in Absinthe. |

### Inventory Items

| Action | Method | Description |
| --- | --- | --- |
| [Archive Inventory Item](actions/archive-inventory-item.md) | DELETE | Archives a reward item in an Absinthe campaign. |
| [Create Inventory Item](actions/create-inventory-item.md) | POST | Creates a reward item in an Absinthe campaign. |
| [List Active Inventory Items](actions/list-active-inventory-items.md) | GET | Retrieves active reward items from an Absinthe campaign. |
| [List Inventory Items](actions/list-inventory-items.md) | GET | Retrieves reward items from an Absinthe campaign. |
| [Update Inventory Item](actions/update-inventory-item.md) | PUT | Updates a reward item in an Absinthe campaign. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Claim Badge](actions/claim-badge.md) | POST | Claims a badge for a user in Absinthe. |
| [Create Badge](actions/create-badge.md) | POST | Creates a new badge in Absinthe. |
| [Delete Badge](actions/delete-badge.md) | DELETE | Deletes a badge by setting it inactive in Absinthe. |
| [Get Badge](actions/get-badge.md) | GET | Retrieves details for a badge from Absinthe. |
| [Get Badge Status](actions/get-badge-status.md) | GET | Retrieves badge eligibility and claim status from Absinthe. |
| [List Badges](actions/list-badges.md) | GET | Retrieves badges from an Absinthe campaign. |
| [Update Badge](actions/update-badge.md) | PUT | Updates an existing badge in Absinthe. |
| [Upload Badge Image](actions/upload-badge-image.md) | POST | Uploads a badge image to Absinthe. |

### Scorecards

| Action | Method | Description |
| --- | --- | --- |
| [Get Leaderboard](actions/get-leaderboard.md) | GET | Retrieves a campaign leaderboard from Absinthe. |
| [Get Leaderboard Stats](actions/get-leaderboard-stats.md) | GET | Retrieves leaderboard metrics for a campaign in Absinthe. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Identities](actions/get-user-identities.md) | GET | Retrieves a user's identities from Absinthe. |
| [Get User Point Sources](actions/get-user-point-sources.md) | GET | Retrieves a user's earned points by source in Absinthe. |
| [Get User Scores](actions/get-user-scores.md) | GET | Retrieves a user's scores and rank from Absinthe. |
| [Get User XP Balance](actions/get-user-xp-balance.md) | GET | Retrieves a user's XP balance from Absinthe. |
| [Resolve Identity to User ID](actions/resolve-identity-to-user-id.md) | GET | Finds a user ID in Absinthe by identity. |

