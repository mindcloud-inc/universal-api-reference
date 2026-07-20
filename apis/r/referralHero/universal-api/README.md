# <img src="https://images.mindcloud.co/apps/icons/referral-hero_1774450067842.png" alt="ReferralHero logo" width="28" height="28"> ReferralHero: Universal API

Manage referral campaigns, subscribers, rewards, and coupons

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/referralHero/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://referralhero.com/
- **Vendor API docs:** https://support.referralhero.com/integrate/rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lists](actions/list-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Coupons

| Action | Method | Description |
| --- | --- | --- |
| [Create Coupons](actions/create-coupons.md) | POST | Creates coupons in ReferralHero. |
| [List Coupons](actions/list-coupons.md) | GET | Retrieves coupons from a coupon group in ReferralHero. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Coupon Group](actions/create-coupon-group.md) | POST | Creates a coupon group in ReferralHero. |
| [List Coupon Groups](actions/list-coupon-groups.md) | GET | Retrieves coupon groups from ReferralHero. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in ReferralHero. |
| [List Lists](actions/list-lists.md) | GET | Retrieves lists from ReferralHero. |

### Reward

| Action | Method | Description |
| --- | --- | --- |
| [List List Rewards](actions/list-list-rewards.md) | GET | Retrieves rewards for a list in ReferralHero. |
| [List Rewards for All Subscribers](actions/list-rewards-for-all-subscribers.md) | GET | Retrieves all subscriber rewards for a list in ReferralHero. |
| [List Subscriber Rewards](actions/list-subscriber-rewards.md) | GET | Retrieves rewards unlocked by a subscriber in ReferralHero. |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscriber](actions/add-subscriber.md) | POST | Creates a new subscriber in ReferralHero. |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE | Deletes an existing subscriber from ReferralHero. |
| [Get List Leaderboard](actions/get-list-leaderboard.md) | GET | Retrieves a list leaderboard from ReferralHero. |
| [List All Level 2 Referrals](actions/list-all-level2-referrals.md) | GET | Retrieves all level 2 referrals from ReferralHero. |
| [List Level 1 Referrals](actions/list-level1-referrals.md) | GET | Retrieves level 1 referrals from ReferralHero. |
| [List Level 2 Referrals](actions/list-level2-referrals.md) | GET | Retrieves level 2 referrals from ReferralHero. |
| [List Level 3 Referrals](actions/list-level3-referrals.md) | GET | Retrieves level 3 referrals from ReferralHero. |
| [List Referred Subscribers](actions/list-referred-subscribers.md) | GET | Retrieves referred subscribers from ReferralHero. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscribers from a list in ReferralHero. |
| [Retrieve Subscriber by Email](actions/retrieve-subscriber-by-email.md) | GET | Retrieves a subscriber from ReferralHero by email address. |
| [Retrieve Subscriber by ID](actions/retrieve-subscriber-by-id.md) | GET | Retrieves a subscriber from ReferralHero by ID. |
| [Retrieve Subscriber by MWR](actions/retrieve-subscriber-by-mwr.md) | GET | Finds a subscriber in ReferralHero by MWR. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in ReferralHero. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Track Bulk Transactions](actions/track-bulk-transactions.md) | POST | Creates bulk subscriber transactions in ReferralHero. |
| [Track Single Transaction](actions/track-single-transaction.md) | POST | Creates a transaction for a subscriber in ReferralHero. |

