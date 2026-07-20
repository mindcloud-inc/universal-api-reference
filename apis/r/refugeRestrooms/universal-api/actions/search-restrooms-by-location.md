# Refuge Restrooms: Search Restrooms by Location



```
GET https://connect.mindcloud.co/v1/universal/refugeRestrooms/latest/actions/search-restrooms-by-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refuge Restrooms `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/refugeRestrooms/latest/actions/search-restrooms-by-location?connectionId=$CONNECTION_ID&limit=25&offset=0&lat=1&lng=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "lat": "1",
  "lng": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/refugeRestrooms/latest/actions/search-restrooms-by-location?${params}`, {
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
| `lat` | number | yes | Latitude to search around. |
| `lng` | number | yes | Longitude to search around. |
| `ada` | boolean | no | Only return restrooms that are ADA accessible. |
| `unisex` | boolean | no | Only return restrooms that are unisex. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resultOffset` | number | no | Pad a number of results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessible": true,
      "approved": true,
      "bearing": "string",
      "changing_table": true,
      "city": "string",
      "comment": "string",
      "country": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "directions": "string",
      "distance": 1,
      "downvote": 1,
      "edit_id": 1,
      "id": 1,
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "state": "string",
      "street": "string",
      "unisex": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "upvote": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessible` | boolean |  |
| `approved` | boolean |  |
| `bearing` | string |  |
| `changing_table` | boolean |  |
| `city` | string |  |
| `comment` | string |  |
| `country` | string |  |
| `created_at` | date |  |
| `directions` | string |  |
| `distance` | number |  |
| `downvote` | number |  |
| `edit_id` | number |  |
| `id` | number |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `name` | string |  |
| `state` | string |  |
| `street` | string |  |
| `unisex` | boolean |  |
| `updated_at` | date |  |
| `upvote` | number |  |

## Native endpoint

Through the native Refuge Restrooms API, this operation is `GET /v1/restrooms/by_location` (base URL `https://www.refugerestrooms.org/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-restrooms-by-location.md) for the provider-specific parameters and requirements.

