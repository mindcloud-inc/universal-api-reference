# WiserReview: Get Product Review Data

Retrieves product review data from WiserReview.

```
GET https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/get-product-review-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WiserReview `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/get-product-review-data?connectionId=$CONNECTION_ID&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/get-product-review-data?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes | Product ID for which to retrieve review data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "arrimg": [
        "string"
      ],
      "arrvdo": [
        "string"
      ],
      "cn": "string",
      "createdAt": "string",
      "ct": "string",
      "Id": "string",
      "ircmnd": true,
      "ivrfd": true,
      "pid": "string",
      "pn": "string",
      "rtng": 1,
      "rttl": "string",
      "rtxt": "string",
      "st": "string",
      "udt": "string",
      "un": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `arrimg` | array<string> | Review image URLs. |
| `arrvdo` | array<string> | Review video URLs. |
| `cn` | string | Reviewer country. |
| `createdAt` | string | Record creation timestamp. |
| `ct` | string | Reviewer city. |
| `Id` | string | Unique review identifier. |
| `ircmnd` | boolean | Whether the reviewer recommends the product. |
| `ivrfd` | boolean | Whether the review is verified. |
| `pid` | string | Product identifier associated with the review. |
| `pn` | string | Product name. |
| `rtng` | number | Rating value. |
| `rttl` | string | Review title. |
| `rtxt` | string | Review text content. |
| `st` | string | Reviewer state or region. |
| `udt` | string | Last update timestamp. |
| `un` | string | Reviewer display name. |

## Native endpoint

Through the native WiserReview API, this operation is `POST https://rs.wiserreview.com/api/v1/getProductReviewData` (base URL `https://api.wiserreview.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-review-data.md) for the provider-specific parameters and requirements.

