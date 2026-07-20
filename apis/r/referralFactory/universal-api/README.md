# <img src="https://images.mindcloud.co/apps/icons/referral-factory_1774034364927.png" alt="Referral Factory logo" width="28" height="28"> Referral Factory: Universal API

Manage referral campaigns, users, and rewards

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/referralFactory/latest
- **Category:** Marketing
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://referral-factory.com
- **Vendor API docs:** https://developers.referral-factory.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Campaigns](actions/list-campaigns.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralFactory/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Referral Factory. |
| [Retrieve Campaign](actions/retrieve-campaign.md) | GET | Retrieves a campaign from Referral Factory. |
| [Search Campaigns](actions/search-campaigns.md) | GET | Finds campaigns in Referral Factory by search criteria. |

### Due Reward

| Action | Method | Description |
| --- | --- | --- |
| [List Due Rewards](actions/list-due-rewards.md) | GET | Retrieves due rewards from Referral Factory by metric. |
| [Search Due Rewards](actions/search-due-rewards.md) | GET | Finds due rewards in Referral Factory by metric. |

### Issued Reward

| Action | Method | Description |
| --- | --- | --- |
| [List Issued Rewards](actions/list-issued-rewards.md) | GET | Retrieves issued rewards from Referral Factory by metric. |
| [Search Issued Rewards](actions/search-issued-rewards.md) | GET | Finds issued rewards in Referral Factory by metric. |

### Reward

| Action | Method | Description |
| --- | --- | --- |
| [List Rewards](actions/list-rewards.md) | GET | Retrieves rewards from Referral Factory by metric. |
| [Search Rewards](actions/search-rewards.md) | GET | Finds rewards in Referral Factory by metric. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from Referral Factory. |
| [Search Users](actions/search-users.md) | GET | Finds users in Referral Factory by search criteria. |

