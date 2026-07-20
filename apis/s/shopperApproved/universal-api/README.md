# <img src="https://images.mindcloud.co/apps/icons/icon-256x256_1774444002759.png" alt="Shopper Approved logo" width="28" height="28"> Shopper Approved: Universal API

Pull reviews, product reviews, and aggregate ratings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shopperApproved/latest
- **Category:** Commerce
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.shopperapproved.com/
- **Vendor API docs:** https://api.shopperapproved.com/ui/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Reviews](actions/list-reviews.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/list-reviews?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Product Aggregate

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Aggregate Statistics](actions/get-product-aggregate-statistics.md) | GET | Retrieves product aggregate statistics from Shopper Approved. |
| [Get Product Aggregate Statistics by Product ID](actions/get-product-aggregate-statistics-by-product-id.md) | GET | Retrieves product aggregate statistics from Shopper Approved by product ID. |

### Product Review

| Action | Method | Description |
| --- | --- | --- |
| [List Product Reviews](actions/list-product-reviews.md) | GET | Retrieves product reviews from Shopper Approved. |
| [List Product Reviews by Product or Parent ID](actions/list-product-reviews-by-product-or-parent-id.md) | GET | Retrieves product reviews from Shopper Approved by product ID. |

### Review

| Action | Method | Description |
| --- | --- | --- |
| [Create Review Entry](actions/create-review-entry.md) | POST | Creates a new review entry in Shopper Approved. |
| [Get Review](actions/get-review.md) | GET | Retrieves a review from Shopper Approved by ID. |
| [List Reviews](actions/list-reviews.md) | GET | Retrieves reviews from Shopper Approved. |
| [Update or Cancel Review](actions/update-or-cancel-review.md) | PUT | Updates or cancels a review in Shopper Approved. |

### Review Aggregate

| Action | Method | Description |
| --- | --- | --- |
| [Get Review Aggregate Statistics](actions/get-review-aggregate-statistics.md) | GET | Retrieves review aggregate statistics from Shopper Approved. |

