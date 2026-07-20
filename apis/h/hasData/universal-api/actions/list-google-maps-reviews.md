# HasData: List Google Maps Reviews

Retrieves Google Maps reviews from HasData.

```
GET https://connect.mindcloud.co/v1/universal/hasData/latest/actions/list-google-maps-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HasData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/list-google-maps-reviews?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/list-google-maps-reviews?${params}`, {
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
| `dataId` | string | no | Google Maps data ID. Either Data ID or Place ID should be set. |
| `nextPageToken` | string | no | Token for the next page of reviews. |
| `placeId` | string | no | Google Maps place ID. Either Data ID or Place ID should be set. |
| `sortBy` | string | no | Sorting option for reviews. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "placeInfo": {},
      "requestMetadata": {},
      "reviews": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object |  |
| `placeInfo` | object |  |
| `requestMetadata` | object |  |
| `reviews` | array<object> |  |

## Native endpoint

Through the native HasData API, this operation is `GET /scrape/google-maps/reviews` (base URL `https://api.hasdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-google-maps-reviews.md) for the provider-specific parameters and requirements.

