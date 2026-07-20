# <img src="https://images.mindcloud.co/apps/icons/climbo20_1774462422075.png" alt="Climbo 2.0 logo" width="28" height="28"> Climbo 2.0: Universal API

Manage Climbo agency clients, plans, and webhook subscriptions through the public Climbo API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/climbo20/latest
- **Category:** Marketing
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.climbo.com/
- **Vendor API docs:** https://climbo.readme.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Plans](actions/list-plans.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/list-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Add Client](actions/add-client.md) | POST | Creates a new client in Climbo 2.0. |
| [Change Client Plan](actions/change-client-plan.md) | PUT | Updates a client's plan in Climbo 2.0. |
| [Change Client Status](actions/change-client-status.md) | PUT | Updates a client's status in Climbo 2.0. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes a client from Climbo 2.0. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Climbo 2.0. |
| [List Clients](actions/list-clients.md) | GET | Retrieves agency clients from Climbo 2.0. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [Get Plan](actions/get-plan.md) | GET | Retrieves a subscription plan from Climbo 2.0. |
| [List Plans](actions/list-plans.md) | GET | Retrieves subscription plans from Climbo 2.0. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a webhook subscription in Climbo 2.0. |
| [Delete Subscription](actions/delete-subscription.md) | DELETE | Deletes a webhook subscription from Climbo 2.0. |

