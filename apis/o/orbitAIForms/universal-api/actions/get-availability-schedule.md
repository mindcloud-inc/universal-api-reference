# Orbit AI (Forms): Get Availability Schedule



```
GET https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/get-availability-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orbit AI (Forms) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/get-availability-schedule?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/get-availability-schedule?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "date_overrides": [
        {}
      ],
      "id": "string",
      "is_default": true,
      "name": "Ava Chen",
      "rules": [
        {}
      ],
      "timezone": "string",
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
| `created_at` | date |  |
| `date_overrides` | array<object> |  |
| `id` | string |  |
| `is_default` | boolean |  |
| `name` | string |  |
| `rules` | array<object> |  |
| `timezone` | string |  |
| `updated_at` | date |  |
| `user_id` | string |  |

## Native endpoint

Through the native Orbit AI (Forms) API, this operation is `GET /api/v1/availability-schedules/:id` (base URL `https://orbitforms.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-availability-schedule.md) for the provider-specific parameters and requirements.

