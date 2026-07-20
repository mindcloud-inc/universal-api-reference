# ScrapingDog: List Google Maps Photos

Retrieves Google Maps photos through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/list-google-maps-photos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/list-google-maps-photos?connectionId=$CONNECTION_ID&dataId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/list-google-maps-photos?${params}`, {
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
      "categories": {
        "id": "string",
        "name": "Ava Chen"
      },
      "photos": {
        "image": "string",
        "thumbnail": "string"
      },
      "scrapingdog_pagination": {
        "next": "string",
        "next_page_token": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<object> |  |
| `categories.id` | string |  |
| `categories.name` | string |  |
| `photos` | array<object> |  |
| `photos.image` | string |  |
| `photos.thumbnail` | string |  |
| `scrapingdog_pagination` | object |  |
| `scrapingdog_pagination.next` | string |  |
| `scrapingdog_pagination.next_page_token` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_maps/photos` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-google-maps-photos.md) for the provider-specific parameters and requirements.

