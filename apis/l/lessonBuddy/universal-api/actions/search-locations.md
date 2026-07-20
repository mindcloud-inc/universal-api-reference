# LessonBuddy: Search Locations

Finds locations in LessonBuddy near an address.

```
GET https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/search-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LessonBuddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/search-locations?connectionId=$CONNECTION_ID&address=string&distance=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string",
  "distance": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/search-locations?${params}`, {
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
| `address` | string | yes | Address string used for location search. |
| `distance` | number | yes | Distance for the location search. |

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

Through the native LessonBuddy API, this operation is `POST /v2/location/locations/search` (base URL `https://api.lessonbuddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-locations.md) for the provider-specific parameters and requirements.

