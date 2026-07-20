# ScrapingDog: Get Google Maps Place Details

Retrieves Google Maps place details through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-maps-place-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-maps-place-details?connectionId=$CONNECTION_ID&dataId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-maps-place-details?${params}`, {
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
| `dataId` | string | yes | Google Maps data_id value for the place to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "place_results": {
        "adderss": "string",
        "data_id": "string",
        "extensions": {
          "service_options": [
            "string"
          ]
        },
        "gps_coordinates": {
          "latitude": 1,
          "longitude": 1
        },
        "order_online": [
          "string"
        ],
        "phone": "string",
        "place_id": "string",
        "provider_id": "string",
        "rating": 1,
        "rating_summary": {
          "amount": 1,
          "stars": 1
        },
        "reviews": 1,
        "service_options": {
          "delivery": true,
          "dine-in": true,
          "onsite_services": true,
          "takeout": true
        },
        "thumbmail": "string",
        "title": "string",
        "type": [
          "string"
        ],
        "type_ids": [
          "string"
        ],
        "unsupported_extensions": {
          "service_options": [
            "string"
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `place_results` | object |  |
| `place_results.adderss` | string |  |
| `place_results.data_id` | string |  |
| `place_results.extensions` | array<object> |  |
| `place_results.extensions.service_options` | array<string> |  |
| `place_results.gps_coordinates` | object |  |
| `place_results.gps_coordinates.latitude` | number |  |
| `place_results.gps_coordinates.longitude` | number |  |
| `place_results.order_online` | array<string> |  |
| `place_results.phone` | string |  |
| `place_results.place_id` | string |  |
| `place_results.provider_id` | string |  |
| `place_results.rating` | number |  |
| `place_results.rating_summary` | array<object> |  |
| `place_results.rating_summary.amount` | number |  |
| `place_results.rating_summary.stars` | number |  |
| `place_results.reviews` | number |  |
| `place_results.service_options` | object |  |
| `place_results.service_options.delivery` | boolean |  |
| `place_results.service_options.dine-in` | boolean |  |
| `place_results.service_options.onsite_services` | boolean |  |
| `place_results.service_options.takeout` | boolean |  |
| `place_results.thumbmail` | string |  |
| `place_results.title` | string |  |
| `place_results.type` | array<string> |  |
| `place_results.type_ids` | array<string> |  |
| `place_results.unsupported_extensions` | array<object> |  |
| `place_results.unsupported_extensions.service_options` | array<string> |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_maps/places` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-google-maps-place-details.md) for the provider-specific parameters and requirements.

