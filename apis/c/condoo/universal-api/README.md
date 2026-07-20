# <img src="https://images.mindcloud.co/apps/icons/condoo_1776692521807.png" alt="condoo logo" width="28" height="28"> condoo: Universal API

Manage analytics websites, visitors, goals, and reporting

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/condoo/latest
- **Category:** Marketing
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://trk.condoo.systems/en/
- **Vendor API docs:** https://trk.condoo.systems/en/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve User](actions/retrieve-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Account Log

| Action | Method | Description |
| --- | --- | --- |
| [List Account Logs](actions/list-account-logs.md) | GET | Retrieves account logs from condoo. |

### Account Payment

| Action | Method | Description |
| --- | --- | --- |
| [List Account Payments](actions/list-account-payments.md) | GET | Retrieves account payments from condoo. |
| [Retrieve Account Payment](actions/retrieve-account-payment.md) | GET | Retrieves an account payment from condoo. |

### Custom Domain

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Domain](actions/create-custom-domain.md) | POST | Creates a new custom domain in condoo. |
| [Delete Custom Domain](actions/delete-custom-domain.md) | DELETE | Deletes an existing custom domain from condoo. |
| [List Custom Domains](actions/list-custom-domains.md) | GET | Retrieves custom domains from condoo. |
| [Retrieve Custom Domain](actions/retrieve-custom-domain.md) | GET | Retrieves a custom domain from condoo. |
| [Update Custom Domain](actions/update-custom-domain.md) | PUT | Updates an existing custom domain in condoo. |

### Goal

| Action | Method | Description |
| --- | --- | --- |
| [Create Goal](actions/create-goal.md) | POST | Creates a new goal in condoo. |
| [Delete Goal](actions/delete-goal.md) | DELETE | Deletes an existing goal from condoo. |
| [List Goals](actions/list-goals.md) | GET | Retrieves goals from condoo. |
| [Retrieve Goal](actions/retrieve-goal.md) | GET | Retrieves a goal from condoo. |
| [Update Goal](actions/update-goal.md) | PUT | Updates an existing goal in condoo. |

### Goal Conversion

| Action | Method | Description |
| --- | --- | --- |
| [Create Goal Conversion](actions/create-goal-conversion.md) | POST | Creates a new goal conversion in condoo. |
| [Delete Goal Conversion](actions/delete-goal-conversion.md) | DELETE | Deletes an existing goal conversion from condoo. |
| [List Goal Conversions](actions/list-goal-conversions.md) | GET | Retrieves goal conversions from condoo. |
| [Retrieve Goal Conversion](actions/retrieve-goal-conversion.md) | GET | Retrieves a goal conversion from condoo. |
| [Update Goal Conversion](actions/update-goal-conversion.md) | PUT | Updates an existing goal conversion in condoo. |

### Pageview

| Action | Method | Description |
| --- | --- | --- |
| [Create Pageview](actions/create-pageview.md) | POST | Creates a new pageview in condoo. |
| [Delete Pageview](actions/delete-pageview.md) | DELETE | Deletes an existing pageview from condoo. |
| [List Pageviews](actions/list-pageviews.md) | GET | Retrieves pageviews from condoo. |
| [Retrieve Pageview](actions/retrieve-pageview.md) | GET | Retrieves a pageview from condoo. |
| [Update Pageview](actions/update-pageview.md) | PUT | Updates an existing pageview in condoo. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve User](actions/retrieve-user.md) | GET | Retrieves the current user from condoo. |

### Visitor

| Action | Method | Description |
| --- | --- | --- |
| [Delete Visitor](actions/delete-visitor.md) | DELETE | Deletes an existing visitor from condoo. |
| [List Visitors](actions/list-visitors.md) | GET | Retrieves visitors from condoo. |
| [Retrieve Visitor](actions/retrieve-visitor.md) | GET | Retrieves a visitor from condoo. |
| [Update Visitor](actions/update-visitor.md) | PUT | Updates an existing visitor in condoo. |

### Website

| Action | Method | Description |
| --- | --- | --- |
| [Create Website](actions/create-website.md) | POST | Creates a new website in condoo. |
| [Delete Website](actions/delete-website.md) | DELETE | Deletes an existing website from condoo. |
| [List Websites](actions/list-websites.md) | GET | Retrieves websites from condoo. |
| [Retrieve Website](actions/retrieve-website.md) | GET | Retrieves a website from condoo. |
| [Update Website](actions/update-website.md) | PUT | Updates an existing website in condoo. |

### Website Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Website Statistics](actions/retrieve-website-statistics.md) | GET | Retrieves website statistics from condoo. |

