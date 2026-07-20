# Get Star Ratings with WiserReview

Retrieves star ratings for a product from WiserReview.

## Endpoint

- **Method:** `POST`
- **Path:** `https://rs.wiserreview.com/api/v1/getStarRating`
- **Base URL:** `https://api.wiserreview.com/api/v1`
- **Official documentation:** [Get Star Ratings](https://apidocs.wiserreview.com/star-rating-26671212e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listProductId[]` | body | `array<string>` | yes | List of product IDs for which to retrieve star ratings. |
