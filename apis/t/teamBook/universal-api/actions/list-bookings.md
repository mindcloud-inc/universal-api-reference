# TeamBook: List Bookings

Retrieves all booking records from TeamBook.

```
GET https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/list-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeamBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/list-bookings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/list-bookings?${params}`, {
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
      "comments": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "duration": "string",
      "id": "string",
      "location": 1,
      "order": "string",
      "project_id": "string",
      "start_time": "string",
      "team_id": "string",
      "tentative": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | string |  |
| `created_at` | date |  |
| `date` | date |  |
| `duration` | string |  |
| `id` | string |  |
| `location` | number |  |
| `order` | string |  |
| `project_id` | string |  |
| `start_time` | string |  |
| `team_id` | string |  |
| `tentative` | string |  |
| `updated_at` | date |  |
| `user_id` | string |  |

## Native endpoint

Through the native TeamBook API, this operation is `GET /bookings` (base URL `https://web.teambookapp.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bookings.md) for the provider-specific parameters and requirements.

