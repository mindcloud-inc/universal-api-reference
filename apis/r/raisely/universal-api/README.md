# <img src="https://images.mindcloud.co/apps/icons/raisely_1773623610471.png" alt="Raisely logo" width="28" height="28"> Raisely: Universal API

Manage Raisely campaigns, profiles, donations, users, and subscriptions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/raisely/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.raisely.com/
- **Vendor API docs:** https://developers.raisely.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Campaigns](actions/list-campaigns.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Raisely. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Raisely. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in Raisely. |

### Donation

| Action | Method | Description |
| --- | --- | --- |
| [Create Donation](actions/create-donation.md) | POST | Creates a new donation in Raisely. |
| [Get Donation](actions/get-donation.md) | GET | Retrieves a donation from Raisely. |
| [List Campaign Donations](actions/list-campaign-donations.md) | GET | Retrieves donations from a Raisely campaign. |
| [List Donations](actions/list-donations.md) | GET | Retrieves donations from Raisely. |
| [List Subscription Donations](actions/list-subscription-donations.md) | GET | Retrieves donations from a Raisely subscription. |
| [Resend Donation Receipt](actions/resend-donation-receipt.md) | PUT | Resends a donation receipt from Raisely. |
| [Update Donation](actions/update-donation.md) | PUT | Updates an existing donation in Raisely. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [List Profile Members](actions/list-profile-members.md) | GET | Retrieves members from a Raisely profile. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET | Retrieves a profile from Raisely. |
| [List Campaign Profiles](actions/list-campaign-profiles.md) | GET | Retrieves profiles from a Raisely campaign. |
| [List Profiles](actions/list-profiles.md) | GET | Retrieves profiles from Raisely. |
| [Update Profile](actions/update-profile.md) | PUT | Updates an existing profile in Raisely. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a new subscription in Raisely. |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves a subscription from Raisely. |
| [List Campaign Subscriptions](actions/list-campaign-subscriptions.md) | GET | Retrieves subscriptions from a Raisely campaign. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from Raisely. |
| [Update Subscription](actions/update-subscription.md) | PUT | Updates an existing subscription in Raisely. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Raisely. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Raisely. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Raisely. |
| [Upsert User](actions/upsert-user.md) | PUT | Finds a user in Raisely, or creates one if no match is found. |

