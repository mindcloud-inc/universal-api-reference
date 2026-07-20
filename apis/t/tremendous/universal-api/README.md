# <img src="https://images.mindcloud.co/apps/icons/icon-144x144_1777311565692.png" alt="Tremendous logo" width="28" height="28"> Tremendous: Universal API

Send rewards, payouts, and incentives globally

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tremendous/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tremendous.com
- **Vendor API docs:** https://developers.tremendous.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tremendous/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in Tremendous. |
| [Retrieve Campaign](actions/get-campaign.md) | GET | Retrieves a specific campaign from Tremendous. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Tremendous. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in Tremendous. |

### Funding Source

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Funding Source](actions/get-funding-source.md) | GET | Retrieves a specific funding source from Tremendous. |
| [List Funding Sources](actions/list-funding-sources.md) | GET | Retrieves funding sources from Tremendous. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Member](actions/get-member.md) | GET | Retrieves a specific member from Tremendous. |
| [List Members](actions/list-members.md) | GET | Retrieves members from Tremendous. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Tremendous. |
| [Retrieve Order](actions/get-order.md) | GET | Retrieves a specific order from Tremendous. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Tremendous. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Organization](actions/get-organization.md) | GET |  |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Tremendous. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Product](actions/get-product.md) | GET | Retrieves a specific product from Tremendous. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Tremendous. |

### Reward

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Reward](actions/get-reward.md) | GET | Retrieves a specific reward from Tremendous. |
| [List Rewards](actions/list-rewards.md) | GET | Retrieves rewards from Tremendous. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Tremendous. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Tremendous. |
| [Retrieve Webhook](actions/get-webhook.md) | GET | Retrieves a specific webhook from Tremendous. |

