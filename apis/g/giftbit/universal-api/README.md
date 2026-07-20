# <img src="https://images.mindcloud.co/apps/icons/giftbit-icon-filled-256_1774470962763.png" alt="Giftbit logo" width="28" height="28"> Giftbit: Universal API

Send and manage digital rewards, gift cards, and payouts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/giftbit/latest
- **Category:** Commerce
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.giftbit.com
- **Vendor API docs:** https://www.giftbit.com/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Ping](actions/ping.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Brand

| Action | Method | Description |
| --- | --- | --- |
| [List Brands](actions/list-brands.md) | GET | Lists available reward brands in Giftbit. |
| [Retrieve Brand](actions/retrieve-brand.md) | GET | Retrieves a reward brand from Giftbit. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign Order](actions/create-campaign-order.md) | POST | Creates a Giftbit campaign order for emailed or shortlink rewards. |
| [Retrieve Order by ID](actions/retrieve-order-by-id.md) | GET | Retrieves a Giftbit order by ID. |

### Direct Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Direct Link Order](actions/create-direct-link-order.md) | POST | Creates a direct link reward order in Giftbit. |

### Funds

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Funding Information](actions/retrieve-funding-information.md) | GET | Retrieves your Giftbit account balance details. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Link URLs](actions/get-link-urls.md) | GET | Retrieves generated reward links for a Giftbit order. |

### Ping

| Action | Method | Description |
| --- | --- | --- |
| [Ping](actions/ping.md) | GET | Tests your Giftbit authentication and API health. |

### Region

| Action | Method | Description |
| --- | --- | --- |
| [List Regions](actions/list-regions.md) | GET | Lists reward regions available in Giftbit. |

### Reward

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Reward](actions/cancel-reward.md) | DELETE | Cancels an unclaimed reward in Giftbit. |
| [Create Embedded Reward](actions/create-embedded-reward.md) | POST | Creates an embedded Giftbit reward for immediate in-app delivery. |
| [List Rewards](actions/list-rewards.md) | GET | Lists rewards in your Giftbit account. |
| [Resend Reward](actions/resend-reward.md) | PUT | Resends a reward to its recipient in Giftbit. |
| [Retrieve Reward](actions/retrieve-reward.md) | GET | Retrieves a reward by UUID from Giftbit. |

