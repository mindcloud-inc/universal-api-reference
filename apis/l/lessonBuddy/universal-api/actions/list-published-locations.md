# LessonBuddy: List Published Locations

Retrieves published locations from LessonBuddy.

```
GET https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/list-published-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LessonBuddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/list-published-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/list-published-locations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "hours": [
        {}
      ],
      "id": 1,
      "mapUrl": "https://example.com",
      "name": "Ava Chen",
      "openDate": "2026-05-07T12:00:00.000Z",
      "phoneNumber": "string",
      "regionSlug": "string",
      "slug": "string",
      "timezone": "string"
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
| `hours` | array<object> |  |
| `id` | number |  |
| `mapUrl` | string |  |
| `name` | string |  |
| `openDate` | date |  |
| `phoneNumber` | string |  |
| `regionSlug` | string |  |
| `slug` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native LessonBuddy API, this operation is `GET /v2/location/locations/published` (base URL `https://api.lessonbuddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-published-locations.md) for the provider-specific parameters and requirements.

