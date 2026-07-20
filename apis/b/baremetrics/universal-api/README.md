# <img src="https://images.mindcloud.co/apps/icons/baremetrics_1774898028027.png" alt="Baremetrics logo" width="28" height="28"> Baremetrics: Universal API

Subscription analytics and Baremetrics operational data, including plans, customers, subscriptions, metrics, and segments.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/baremetrics/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://baremetrics.com
- **Vendor API docs:** https://developers.baremetrics.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a customer in Baremetrics. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes a customer from Baremetrics. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Baremetrics. |
| [Show Customer](actions/show-customer.md) | GET | Retrieves a customer from Baremetrics. |
| [Update Customer](actions/update-customer.md) | PUT | Updates a customer in Baremetrics. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [List Sources](actions/list-sources.md) | GET | Retrieves sources from Baremetrics. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Events](actions/list-customer-events.md) | GET | Retrieves customer events from Baremetrics. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Show Customers](actions/show-customers.md) | GET | Retrieves customers for a metric from Baremetrics. |
| [Show Metric](actions/show-metric.md) | GET | Retrieves a metric from Baremetrics. |
| [Show Plan Breakout](actions/show-plan-breakout.md) | GET | Retrieves metric breakdowns by plan from Baremetrics. |
| [Show Summary](actions/show-summary.md) | GET | Retrieves summary metrics from Baremetrics. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment](actions/create-segment.md) | POST | Creates a segment in Baremetrics. |
| [List Fields](actions/list-fields.md) | GET | Retrieves segment fields from Baremetrics. |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments from Baremetrics. |
| [Search Segment](actions/search-segment.md) | GET | Finds segment results in Baremetrics without saving the segment. |
| [Show Segment](actions/show-segment.md) | GET | Retrieves a segment from Baremetrics. |
| [Update Segment](actions/update-segment.md) | PUT | Updates a segment in Baremetrics. |

### Service Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from Baremetrics. |

### Subscription Plans

| Action | Method | Description |
| --- | --- | --- |
| [Create Plan](actions/create-plan.md) | POST | Creates a plan in Baremetrics. |
| [Delete Plan](actions/delete-plan.md) | DELETE | Deletes a plan from Baremetrics. |
| [List Plans](actions/list-plans.md) | GET | Retrieves plans from Baremetrics. |
| [Show Plan](actions/show-plan.md) | GET | Retrieves a plan from Baremetrics. |
| [Update Plan](actions/update-plan.md) | PUT | Updates a plan in Baremetrics. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | PUT | Cancels a subscription in Baremetrics. |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a subscription in Baremetrics. |
| [Delete Subscription](actions/delete-subscription.md) | DELETE | Deletes a subscription from Baremetrics. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from Baremetrics. |
| [Show Subscription](actions/show-subscription.md) | GET | Retrieves a subscription from Baremetrics. |
| [Update Subscription](actions/update-subscription.md) | PUT | Updates a subscription in Baremetrics. |

