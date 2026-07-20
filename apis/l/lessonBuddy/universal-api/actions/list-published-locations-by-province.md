# LessonBuddy: List Published Locations By Province

Retrieves published locations grouped by province in LessonBuddy.

```
GET https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/list-published-locations-by-province
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LessonBuddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/list-published-locations-by-province?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/list-published-locations-by-province?${params}`, {
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
      "id": 1,
      "locations": [
        {}
      ],
      "name": "Ava Chen",
      "shortName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `locations` | array<object> |  |
| `name` | string |  |
| `shortName` | string |  |

## Native endpoint

Through the native LessonBuddy API, this operation is `GET /v2/location/locations/published/by-province` (base URL `https://api.lessonbuddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-published-locations-by-province.md) for the provider-specific parameters and requirements.

