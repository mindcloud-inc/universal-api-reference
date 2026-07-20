# <img src="https://images.mindcloud.co/apps/icons/more-good-reviews_1774558583993.png" alt="More Good Reviews logo" width="28" height="28"> More Good Reviews: Universal API

More Good Reviews helps businesses collect customer reviews, send review requests by email or SMS, manage locations and customer feedback, and export reviews through a REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/moreGoodReviews/latest
- **Category:** Support / Customer Success
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://moregoodreviews.com
- **Vendor API docs:** https://docs.moregoodreviews.com/platform/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreGoodReviews/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Charge

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Charge](actions/create-customer-charge.md) | POST | Creates a customer charge in More Good Reviews. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Customer](actions/create-or-update-customer.md) | POST | Creates a customer in More Good Reviews. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from More Good Reviews. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST | Creates a location in More Good Reviews. |
| [Update Location](actions/update-location.md) | PUT | Updates a location in More Good Reviews. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Messages](actions/list-customer-messages.md) | GET | Retrieves messages for a customer in More Good Reviews. |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages from More Good Reviews. |

### Review

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Reviews](actions/list-customer-reviews.md) | GET | Retrieves reviews for a customer in More Good Reviews. |
| [List Reviews](actions/list-reviews.md) | GET | Retrieves reviews from More Good Reviews. |

### Review Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Review Request](actions/create-review-request.md) | POST | Creates a review request in More Good Reviews. |

