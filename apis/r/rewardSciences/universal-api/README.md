# <img src="https://images.mindcloud.co/apps/icons/reward-sciences_1775039654547.png" alt="Reward Sciences logo" width="28" height="28"> Reward Sciences: Universal API

Reward Sciences helps teams run loyalty and rewards programs through a REST API for activities, users, rewards, redemptions, and bids.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rewardSciences/latest
- **Category:** Marketing
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developers.rewardsciences.com
- **Vendor API docs:** https://developers.rewardsciences.com/api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Reward Categories](actions/list-reward-categories.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/list-reward-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Track Activity](actions/track-activity.md) | POST |  |

### Reward

| Action | Method | Description |
| --- | --- | --- |
| [Get Reward](actions/get-reward.md) | GET |  |
| [List Rewards](actions/list-rewards.md) | GET |  |

### Reward Bid

| Action | Method | Description |
| --- | --- | --- |
| [Bid On Reward](actions/bid-on-reward.md) | POST |  |

### Reward Category

| Action | Method | Description |
| --- | --- | --- |
| [List Reward Categories](actions/list-reward-categories.md) | GET |  |

### Reward Redemption

| Action | Method | Description |
| --- | --- | --- |
| [Redeem Reward](actions/redeem-reward.md) | POST |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User By External Identity](actions/create-user-by-external-identity.md) | POST |  |
| [Get User](actions/get-user.md) | GET |  |
| [Get User By External Identity](actions/get-user-by-external-identity.md) | GET |  |

### User Identity

| Action | Method | Description |
| --- | --- | --- |
| [Assign External Identity To User](actions/assign-external-identity-to-user.md) | POST |  |

