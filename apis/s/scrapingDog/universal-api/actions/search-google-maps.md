# ScrapingDog: Search Google Maps

Retrieves Google Maps search results through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-maps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-maps?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-maps?${params}`, {
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
| `query` | string | yes | Search query to run on Google Maps. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "search_results": {
        "address": "string",
        "data_cid": "string",
        "data_id": "string",
        "description": "string",
        "gps_coordinates": {
          "latitude": 1,
          "longitude": 1
        },
        "hours": "string",
        "open_state": "string",
        "operating_hours": {
          "friday": "string",
          "monday": "string",
          "saturday": "string",
          "sunday": "string",
          "thursday": "string",
          "tuesday": "string",
          "wednesday": "string"
        },
        "phone": "string",
        "photos_link": "https://example.com",
        "place_id": "string",
        "posts_link": "https://example.com",
        "price": "string",
        "provider_id": "string",
        "rating": 1,
        "reviews": 1,
        "reviews_link": "https://example.com",
        "thumbnail": "string",
        "title": "string",
        "type": "string",
        "types": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `search_results` | array<object> |  |
| `search_results.address` | string |  |
| `search_results.data_cid` | string |  |
| `search_results.data_id` | string |  |
| `search_results.description` | string |  |
| `search_results.gps_coordinates` | object |  |
| `search_results.gps_coordinates.latitude` | number |  |
| `search_results.gps_coordinates.longitude` | number |  |
| `search_results.hours` | string |  |
| `search_results.open_state` | string |  |
| `search_results.operating_hours` | object |  |
| `search_results.operating_hours.friday` | string |  |
| `search_results.operating_hours.monday` | string |  |
| `search_results.operating_hours.saturday` | string |  |
| `search_results.operating_hours.sunday` | string |  |
| `search_results.operating_hours.thursday` | string |  |
| `search_results.operating_hours.tuesday` | string |  |
| `search_results.operating_hours.wednesday` | string |  |
| `search_results.phone` | string |  |
| `search_results.photos_link` | string |  |
| `search_results.place_id` | string |  |
| `search_results.posts_link` | string |  |
| `search_results.price` | string |  |
| `search_results.provider_id` | string |  |
| `search_results.rating` | number |  |
| `search_results.reviews` | number |  |
| `search_results.reviews_link` | string |  |
| `search_results.thumbnail` | string |  |
| `search_results.title` | string |  |
| `search_results.type` | string |  |
| `search_results.types` | array<string> |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_maps` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-maps.md) for the provider-specific parameters and requirements.

