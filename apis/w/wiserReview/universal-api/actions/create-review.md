# WiserReview: Create Review

Creates a new review in WiserReview.

```
POST https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/create-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WiserReview `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/create-review" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/create-review', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Reviewer email address. |
| `rating` | number | no | Review rating value. |
| `userName` | string | no | Reviewer display name. |
| `phoneNumber` | string | no | Reviewer phone number. |
| `title` | string | no | Review title. |
| `reviewText` | string | no | Review body text. |
| `reviewerImage` | string | no | Reviewer profile image URL. |
| `reviewImages[]` | array<string> | no | List of review image URLs. |
| `productName` | string | no | Product name associated with the review. |
| `productURL` | string | no | Product page URL. |
| `productId` | string | no | Product identifier associated with the review. |
| `productImageURL` | string | no | Product image URL. |
| `orderId` | string | no | Order identifier associated with the review. |
| `isVerified` | boolean | no | Whether the reviewer is verified. |
| `isRecommended` | boolean | no | Whether the reviewer recommends the product. |
| `youtubeURL` | string | no | YouTube URL associated with the review. |
| `xURL` | string | no | X profile or post URL associated with the review. |
| `linkedinURL` | string | no | LinkedIn URL associated with the review. |
| `instagramURL` | string | no | Instagram URL associated with the review. |
| `city` | string | no | Reviewer city. |
| `state` | string | no | Reviewer state or region. |
| `country` | string | no | Reviewer country. |
| `ipAddress` | string | no | Reviewer IP address. |
| `latitude` | string | no | Latitude associated with the review. |
| `longitude` | string | no | Longitude associated with the review. |
| `skuId` | string | no | SKU identifier associated with the review. |
| `variantId` | string | no | Product variant identifier. |
| `skuTitle` | string | no | SKU title. |
| `companyDesignation` | string | no | Reviewer company designation. |
| `companyName` | string | no | Reviewer company name. |
| `companySiteURL` | string | no | Reviewer company website URL. |
| `companyLogo` | string | no | Reviewer company logo URL. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WiserReview API returns.

## Native endpoint

Through the native WiserReview API, this operation is `POST /createReview` (base URL `https://api.wiserreview.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-review.md) for the provider-specific parameters and requirements.

