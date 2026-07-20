# ScrapingDog: List Google Maps Reviews

Retrieves Google Maps reviews through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/list-google-maps-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/list-google-maps-reviews?connectionId=$CONNECTION_ID&dataId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/list-google-maps-reviews?${params}`, {
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
| `dataId` | string | yes | Google Maps data_id value for the business or place. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "locationDetails": {
        "address": "string",
        "rating": 1,
        "reviews": 1,
        "title": "string"
      },
      "pagination": {
        "next": "string",
        "next_page_token": "string"
      },
      "reviews_results": {
        "date": "string",
        "details": {
          "reservation_recommended": "string",
          "visited_on": "string",
          "wait_time": "string"
        },
        "images": [
          "string"
        ],
        "iso_date": "string",
        "iso_date_of_last_edit": "string",
        "likes": 1,
        "link": "https://example.com",
        "rating": 1,
        "response": {
          "date": "string",
          "iso_date": "string",
          "iso_date_of_last_edit": "string",
          "response_from_owner_string": "string"
        },
        "review_id": "string",
        "snippet": "string",
        "source": "string",
        "user": {
          "contributor_id": 1,
          "link": "https://example.com",
          "local_guide": true,
          "name": "Ava Chen",
          "photos": 1,
          "reviews": 1,
          "thumbnail": "string"
        }
      },
      "topics": {
        "id": "string",
        "keyword": "string",
        "mentions": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `locationDetails` | object |  |
| `locationDetails.address` | string |  |
| `locationDetails.rating` | number |  |
| `locationDetails.reviews` | number |  |
| `locationDetails.title` | string |  |
| `pagination` | object |  |
| `pagination.next` | string |  |
| `pagination.next_page_token` | string |  |
| `reviews_results` | array<object> |  |
| `reviews_results.date` | string |  |
| `reviews_results.details` | object |  |
| `reviews_results.details.reservation_recommended` | string |  |
| `reviews_results.details.visited_on` | string |  |
| `reviews_results.details.wait_time` | string |  |
| `reviews_results.images` | array<string> |  |
| `reviews_results.iso_date` | string |  |
| `reviews_results.iso_date_of_last_edit` | string |  |
| `reviews_results.likes` | number |  |
| `reviews_results.link` | string |  |
| `reviews_results.rating` | number |  |
| `reviews_results.response` | object |  |
| `reviews_results.response.date` | string |  |
| `reviews_results.response.iso_date` | string |  |
| `reviews_results.response.iso_date_of_last_edit` | string |  |
| `reviews_results.response.response_from_owner_string` | string |  |
| `reviews_results.review_id` | string |  |
| `reviews_results.snippet` | string |  |
| `reviews_results.source` | string |  |
| `reviews_results.user` | object |  |
| `reviews_results.user.contributor_id` | number |  |
| `reviews_results.user.link` | string |  |
| `reviews_results.user.local_guide` | boolean |  |
| `reviews_results.user.name` | string |  |
| `reviews_results.user.photos` | number |  |
| `reviews_results.user.reviews` | number |  |
| `reviews_results.user.thumbnail` | string |  |
| `topics` | array<object> |  |
| `topics.id` | string |  |
| `topics.keyword` | string |  |
| `topics.mentions` | number |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_maps/reviews` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-google-maps-reviews.md) for the provider-specific parameters and requirements.

