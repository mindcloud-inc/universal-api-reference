# LessonBuddy: Get Location By ID

Retrieves a location from LessonBuddy by ID.

```
GET https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/get-location-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LessonBuddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/get-location-by-id?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/get-location-by-id?${params}`, {
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
| `id` | number | yes | LessonBuddy location ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressId": 1,
      "closeDate": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "hours": [
        {}
      ],
      "id": 1,
      "mapUrl": "https://example.com",
      "name": "Ava Chen",
      "openDate": "2026-05-07T12:00:00.000Z",
      "organizationId": 1,
      "phoneNumber": "string",
      "publishDate": "2026-05-07T12:00:00.000Z",
      "regionId": 1,
      "regionSlug": "string",
      "slug": "string",
      "timezone": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressId` | number |  |
| `closeDate` | date |  |
| `displayName` | string |  |
| `email` | string |  |
| `hours` | array<object> |  |
| `id` | number |  |
| `mapUrl` | string |  |
| `name` | string |  |
| `openDate` | date |  |
| `organizationId` | number |  |
| `phoneNumber` | string |  |
| `publishDate` | date |  |
| `regionId` | number |  |
| `regionSlug` | string |  |
| `slug` | string |  |
| `timezone` | string |  |
| `type` | string |  |

## Native endpoint

Through the native LessonBuddy API, this operation is `GET /v2/location/locations/:id` (base URL `https://api.lessonbuddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location-by-id.md) for the provider-specific parameters and requirements.

