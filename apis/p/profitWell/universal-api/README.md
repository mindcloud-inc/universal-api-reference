# <img src="https://images.mindcloud.co/apps/icons/idw-m-7fu-gl-1774634976465_1774634982448.png" alt="ProfitWell logo" width="28" height="28"> ProfitWell: Universal API

Track subscription metrics, customers, plans, and retention performance

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/profitWell/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.paddle.com/profitwell-metrics
- **Vendor API docs:** https://classic.paddle.com/profitwell/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company Settings](actions/get-company-settings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/get-company-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Api Status

| Action | Method | Description |
| --- | --- | --- |
| [Get API Status](actions/get-api-status.md) | GET | Retrieves API status from ProfitWell. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Settings](actions/get-company-settings.md) | GET | Retrieves company settings from ProfitWell. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Anonymize Customer By Email](actions/anonymize-customer-by-email.md) | POST | Anonymizes a customer in ProfitWell by email address. |
| [Anonymize Customer By ID](actions/anonymize-customer-by-id.md) | POST | Anonymizes a customer in ProfitWell by customer ID. |
| [Exclude Customer From Metrics](actions/exclude-customer-from-metrics.md) | POST | Excludes a customer from ProfitWell metrics. |
| [Retrieve Customer By ID](actions/retrieve-customer-by-id.md) | GET | Retrieves a customer from ProfitWell by customer ID. |
| [Search Customers](actions/search-customers.md) | GET | Finds customers in ProfitWell. |

### Customer Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Event](actions/create-customer-event.md) | POST | Creates a customer event in ProfitWell. |

### Customer Trait

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Customer Trait](actions/create-or-update-customer-trait.md) | PUT | Creates or updates a customer trait in ProfitWell. |
| [Get Customer Traits](actions/get-customer-traits.md) | GET | Retrieves customer traits from ProfitWell. |
| [Remove Customer Trait](actions/remove-customer-trait.md) | DELETE | Deletes a customer trait from ProfitWell. |

### Customer Trait Category

| Action | Method | Description |
| --- | --- | --- |
| [Remove Trait Category](actions/remove-trait-category.md) | DELETE | Deletes a trait category from ProfitWell. |

### Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Daily Metrics](actions/get-daily-metrics.md) | GET | Retrieves daily metrics from ProfitWell. |
| [Get Monthly Metrics](actions/get-monthly-metrics.md) | GET | Retrieves monthly metrics from ProfitWell. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [Create Plan](actions/create-plan.md) | POST | Creates a plan in ProfitWell. |
| [Get Plan IDs](actions/get-plan-ids.md) | GET | Retrieves plan IDs from ProfitWell. |
| [List Manually-Added Plans](actions/list-manually-added-plans.md) | GET | Retrieves manually added plans from ProfitWell. |
| [Retrieve Plan](actions/retrieve-plan.md) | GET | Retrieves a plan from ProfitWell. |
| [Update Plan](actions/update-plan.md) | PUT | Updates a plan in ProfitWell. |

### Retain

| Action | Method | Description |
| --- | --- | --- |
| [Stop Retain For Customer](actions/stop-retain-for-customer.md) | POST | Stops Retain interventions for a customer in ProfitWell. |

### Retain Customer

| Action | Method | Description |
| --- | --- | --- |
| [List Retain Unsubscribed Customers](actions/list-retain-unsubscribed-customers.md) | GET | Retrieves Retain unsubscribed customers from ProfitWell. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Churn Subscription](actions/churn-subscription.md) | DELETE | Churns a subscription in ProfitWell. |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a subscription in ProfitWell. |
| [Get Subscription History For User](actions/get-subscription-history-for-user.md) | GET | Retrieves subscription history for a user from ProfitWell. |
| [Un-Churn Subscription](actions/un-churn-subscription.md) | PUT | Reactivates a churned subscription in ProfitWell. |
| [Upgrade Or Downgrade Subscription](actions/upgrade-or-downgrade-subscription.md) | PUT | Updates a subscription in ProfitWell. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Delete User](actions/delete-user.md) | DELETE | Deletes a user from ProfitWell. |
| [Update User](actions/update-user.md) | PUT | Updates a user in ProfitWell. |

