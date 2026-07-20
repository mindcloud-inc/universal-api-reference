# ScrapingDog: List Google Maps Posts

Retrieves Google Maps posts through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/list-google-maps-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/list-google-maps-posts?connectionId=$CONNECTION_ID&dataId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/list-google-maps-posts?${params}`, {
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
      "post_results": {
        "location_details": {
          "logo": "string",
          "name": "Ava Chen"
        },
        "next_page_token": "string",
        "post_data": {
          "date": "string",
          "description": "string",
          "image": "string",
          "link": "https://example.com"
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
| `post_results` | object |  |
| `post_results.location_details` | object |  |
| `post_results.location_details.logo` | string |  |
| `post_results.location_details.name` | string |  |
| `post_results.next_page_token` | string |  |
| `post_results.post_data` | array<object> |  |
| `post_results.post_data.date` | string |  |
| `post_results.post_data.description` | string |  |
| `post_results.post_data.image` | string |  |
| `post_results.post_data.link` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_maps/posts` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-google-maps-posts.md) for the provider-specific parameters and requirements.

