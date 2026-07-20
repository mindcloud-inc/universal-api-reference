# <img src="https://images.mindcloud.co/apps/icons/referral-rock_1774029053739.png" alt="Referral Rock logo" width="28" height="28"> Referral Rock: Universal API

Manage referral programs, members, referrals, rewards, and payouts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/referralRock/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://referralrock.com
- **Vendor API docs:** https://api.referralrock.com/help

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Programs](actions/list-programs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-programs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Create Member](actions/create-member.md) | POST | Creates a new member in Referral Rock. |
| [Delete Members](actions/delete-members.md) | DELETE | Deletes existing members from Referral Rock. |
| [List Members](actions/list-members.md) | GET | Retrieves referral program members from Referral Rock. |
| [Update Members](actions/update-members.md) | PUT | Updates existing members in Referral Rock. |

### Member Access Url

| Action | Method | Description |
| --- | --- | --- |
| [Create Member Access URLs](actions/create-member-access-urls.md) | POST | Creates member share and portal URLs in Referral Rock. |

### Member Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Member Statistics](actions/get-member-statistics.md) | GET | Retrieves member sharing and reward statistics from Referral Rock. |

### Payouts

| Action | Method | Description |
| --- | --- | --- |
| [Create Payout Transactions](actions/create-payout-transactions.md) | POST | Creates payout transactions for pending Referral Rock rewards. |
| [List Payout Transactions](actions/list-payout-transactions.md) | GET | Retrieves payout transactions from Referral Rock. |
| [List Payouts](actions/list-payouts.md) | GET | Retrieves payout records from Referral Rock. |
| [List Pending Payouts](actions/list-pending-payouts.md) | GET | Retrieves pending payouts from Referral Rock. |

### Programs

| Action | Method | Description |
| --- | --- | --- |
| [Get Program](actions/get-program.md) | GET | Retrieves a referral program from Referral Rock by name. |
| [List Programs](actions/list-programs.md) | GET | Retrieves referral programs from Referral Rock. |

### Referral

| Action | Method | Description |
| --- | --- | --- |
| [Create Referral](actions/create-referral.md) | POST | Creates a new referral in Referral Rock from a member referral code. |
| [Delete Referrals](actions/delete-referrals.md) | DELETE | Deletes existing referrals from Referral Rock. |
| [Get Referral](actions/get-referral.md) | GET | Retrieves a referral from Referral Rock by email, referral ID, or external ID. |
| [List Referrals](actions/list-referrals.md) | GET | Retrieves referral records from Referral Rock. |
| [Update Referrals](actions/update-referrals.md) | PUT | Updates existing referrals in Referral Rock. |

### Reward

| Action | Method | Description |
| --- | --- | --- |
| [Create Rewards](actions/create-rewards.md) | POST | Creates new rewards in Referral Rock. |
| [Delete Rewards](actions/delete-rewards.md) | DELETE | Deletes existing rewards from Referral Rock. |
| [Issue Reward](actions/issue-reward.md) | PUT | Issues a specific reward in Referral Rock. |
| [List Rewards](actions/list-rewards.md) | GET | Retrieves reward records from Referral Rock. |
| [Update Rewards](actions/update-rewards.md) | PUT | Updates existing rewards in Referral Rock. |

### Reward Rule

| Action | Method | Description |
| --- | --- | --- |
| [List Reward Rules](actions/list-reward-rules.md) | GET | Retrieves member reward rules from Referral Rock. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Hook](actions/create-hook.md) | POST | Creates a webhook subscription in Referral Rock. |
| [Delete Hook](actions/delete-hook.md) | DELETE | Deletes a webhook subscription from Referral Rock. |

