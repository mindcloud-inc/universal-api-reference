# ScrapingDog: List Amazon Reviews

Retrieves Amazon product reviews through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/list-amazon-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/list-amazon-reviews?connectionId=$CONNECTION_ID&asin=string&domain=string&page=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "asin": "string",
  "domain": "string",
  "page": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/list-amazon-reviews?${params}`, {
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
| `asin` | string | yes | Amazon product identifier. |
| `domain` | string | yes | Amazon top-level domain. |
| `page` | string | yes | Amazon reviews page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actual_reviews": 1,
      "customer_reviews": {
        "date": "string",
        "rating": 1,
        "review": "string",
        "title": "string",
        "user": "string"
      },
      "rating": 1,
      "reviews": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actual_reviews` | number |  |
| `customer_reviews` | array<object> |  |
| `customer_reviews.date` | string |  |
| `customer_reviews.rating` | number |  |
| `customer_reviews.review` | string |  |
| `customer_reviews.title` | string |  |
| `customer_reviews.user` | string |  |
| `rating` | number |  |
| `reviews` | number |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /amazon/reviews` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-amazon-reviews.md) for the provider-specific parameters and requirements.

