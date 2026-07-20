# ScrapingDog: Search Google Local

Retrieves Google Local search results through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-local
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-local?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-local?${params}`, {
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
| `query` | string | yes | Search query for Google Local. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "local_results": {
        "address": "string",
        "description": "string",
        "gps_coordinates": {
          "lat": "string",
          "lng": "string"
        },
        "place_id": "string",
        "place_id_search": "string",
        "price": "string",
        "rating": "string",
        "reviews": "string",
        "thumbnail": "string",
        "title": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `local_results` | array<object> |  |
| `local_results.address` | string |  |
| `local_results.description` | string |  |
| `local_results.gps_coordinates` | object |  |
| `local_results.gps_coordinates.lat` | string |  |
| `local_results.gps_coordinates.lng` | string |  |
| `local_results.place_id` | string |  |
| `local_results.place_id_search` | string |  |
| `local_results.price` | string |  |
| `local_results.rating` | string |  |
| `local_results.reviews` | string |  |
| `local_results.thumbnail` | string |  |
| `local_results.title` | string |  |
| `local_results.type` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_local` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-local.md) for the provider-specific parameters and requirements.

