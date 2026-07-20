# Create Review with WiserReview

Creates a new review in WiserReview.

## Endpoint

- **Method:** `POST`
- **Path:** `/createReview`
- **Base URL:** `https://api.wiserreview.com/api/v1`
- **Official documentation:** [Create Review](https://apidocs.wiserreview.com/create-review-26260657e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Reviewer email address. |
| `rating` | body | `number` | no | Review rating value. |
| `userName` | body | `string` | no | Reviewer display name. |
| `phoneNumber` | body | `string` | no | Reviewer phone number. |
| `title` | body | `string` | no | Review title. |
| `reviewText` | body | `string` | no | Review body text. |
| `reviewerImage` | body | `string` | no | Reviewer profile image URL. |
| `reviewImages[]` | body | `array<string>` | no | List of review image URLs. |
| `productName` | body | `string` | no | Product name associated with the review. |
| `productURL` | body | `string` | no | Product page URL. |
| `productId` | body | `string` | no | Product identifier associated with the review. |
| `productImageURL` | body | `string` | no | Product image URL. |
| `orderId` | body | `string` | no | Order identifier associated with the review. |
| `isVerified` | body | `boolean` | no | Whether the reviewer is verified. |
| `isRecommended` | body | `boolean` | no | Whether the reviewer recommends the product. |
| `youtubeURL` | body | `string` | no | YouTube URL associated with the review. |
| `xURL` | body | `string` | no | X profile or post URL associated with the review. |
| `linkedinURL` | body | `string` | no | LinkedIn URL associated with the review. |
| `instagramURL` | body | `string` | no | Instagram URL associated with the review. |
| `city` | body | `string` | no | Reviewer city. |
| `state` | body | `string` | no | Reviewer state or region. |
| `country` | body | `string` | no | Reviewer country. |
| `ipAddress` | body | `string` | no | Reviewer IP address. |
| `latitude` | body | `string` | no | Latitude associated with the review. |
| `longitude` | body | `string` | no | Longitude associated with the review. |
| `skuId` | body | `string` | no | SKU identifier associated with the review. |
| `variantId` | body | `string` | no | Product variant identifier. |
| `skuTitle` | body | `string` | no | SKU title. |
| `companyDesignation` | body | `string` | no | Reviewer company designation. |
| `companyName` | body | `string` | no | Reviewer company name. |
| `companySiteURL` | body | `string` | no | Reviewer company website URL. |
| `companyLogo` | body | `string` | no | Reviewer company logo URL. |
