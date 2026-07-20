# <img src="https://images.mindcloud.co/apps/icons/icon-256x256_1774895568614.png" alt="WiserReview logo" width="28" height="28"> WiserReview: Universal API

Collect, manage, and display product reviews

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wiserReview/latest
- **Category:** Commerce
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://wiserreview.com
- **Vendor API docs:** https://apidocs.wiserreview.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Reviews](actions/list-reviews.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/list-reviews?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Auth Token

| Action | Method | Description |
| --- | --- | --- |
| [Generate Token](actions/generate-token.md) | GET | Generates an auth token for WiserReview. |

### Product Rating

| Action | Method | Description |
| --- | --- | --- |
| [Get Star Ratings](actions/get-star-ratings.md) | GET | Retrieves star ratings for a product from WiserReview. |

### Review

| Action | Method | Description |
| --- | --- | --- |
| [Create Review](actions/create-review.md) | POST | Creates a new review in WiserReview. |
| [Get Product Review Data](actions/get-product-review-data.md) | GET | Retrieves product review data from WiserReview. |
| [List Reviews](actions/list-reviews.md) | GET | Retrieves reviews from WiserReview. |
| [List Reviews By Product](actions/list-reviews-by-product.md) | GET | Retrieves reviews for a product from WiserReview. |

