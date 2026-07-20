# WiserReview: List Reviews By Product

Retrieves reviews for a product from WiserReview.

```
GET https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/list-reviews-by-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WiserReview `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/list-reviews-by-product?connectionId=$CONNECTION_ID&limit=25&offset=0&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/list-reviews-by-product?${params}`, {
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
| `productId` | string | yes | Unique identifier of the product to fetch related reviews for. |

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
      "e": "string",
      "Id": "string",
      "ircmnd": true,
      "ivrfd": true,
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
| `e` | string | Reviewer email address. |
| `Id` | string | Unique review identifier. |
| `ircmnd` | boolean | Whether the reviewer recommends the product. |
| `ivrfd` | boolean | Whether the review is verified. |
| `rtng` | number | Rating value. |
| `rttl` | string | Review title. |
| `rtxt` | string | Review text content. |
| `st` | string | Reviewer state or region. |
| `udt` | string | Last update timestamp. |
| `un` | string | Reviewer display name. |

## Native endpoint

Through the native WiserReview API, this operation is `GET /reviewsByProduct` (base URL `https://api.wiserreview.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-reviews-by-product.md) for the provider-specific parameters and requirements.

