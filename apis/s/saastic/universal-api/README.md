# <img src="https://images.mindcloud.co/apps/icons/saastic_1776787876420.png" alt="Saastic logo" width="28" height="28"> Saastic: Universal API

Saastic helps teams collect customer reviews, send review requests by email or SMS, manage locations and customer feedback, and export reviews through the More Good Reviews REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/saastic/latest
- **Category:** Support / Customer Success
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://moregoodreviews.com
- **Vendor API docs:** https://docs.moregoodreviews.com/platform/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/saastic/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Charge

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Charge](actions/create-customer-charge.md) | POST | Creates a customer charge in Saastic. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Customer](actions/create-or-update-customer.md) | POST | Creates or updates a customer in Saastic. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Saastic. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST | Creates a new location in Saastic. |
| [Update Location](actions/update-location.md) | PUT | Updates an existing location in Saastic. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Messages](actions/list-customer-messages.md) | GET | Retrieves messages for a customer from Saastic. |

### Review

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Reviews](actions/list-customer-reviews.md) | GET | Retrieves reviews for a customer from Saastic. |
| [List Reviews](actions/list-reviews.md) | GET | Retrieves reviews from Saastic. |

### Review Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Review Request](actions/create-review-request.md) | POST | Creates a review request in Saastic. |

