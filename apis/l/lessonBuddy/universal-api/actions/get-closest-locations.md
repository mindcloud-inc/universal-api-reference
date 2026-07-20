# LessonBuddy: Get Closest Locations

Finds locations in LessonBuddy by distance from coordinates.

```
GET https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/get-closest-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LessonBuddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/get-closest-locations?connectionId=$CONNECTION_ID&latitude=1&longitude=1&radius=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "1",
  "longitude": "1",
  "radius": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/get-closest-locations?${params}`, {
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
| `latitude` | number | yes | Latitude for the center point. |
| `longitude` | number | yes | Longitude for the center point. |
| `radius` | number | yes | Search radius around the latitude and longitude. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "featuredMessage": "string",
      "hours": [
        {}
      ],
      "id": 1,
      "mapUrl": "https://example.com",
      "name": "Ava Chen",
      "openDate": "2026-05-07T12:00:00.000Z",
      "phoneNumber": "string",
      "regionSlug": "string",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `email` | string |  |
| `featuredMessage` | string |  |
| `hours` | array<object> |  |
| `id` | number |  |
| `mapUrl` | string |  |
| `name` | string |  |
| `openDate` | date |  |
| `phoneNumber` | string |  |
| `regionSlug` | string |  |
| `slug` | string |  |

## Native endpoint

Through the native LessonBuddy API, this operation is `GET /v2/location/locations/closest/:latitude/:longitude/:radius` (base URL `https://api.lessonbuddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-closest-locations.md) for the provider-specific parameters and requirements.

