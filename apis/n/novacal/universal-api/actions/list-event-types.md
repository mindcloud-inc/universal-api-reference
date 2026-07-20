# Novacal: List Event Types

Retrieves event types from Novacal.

```
GET https://connect.mindcloud.co/v1/universal/novacal/latest/actions/list-event-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novacal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/novacal/latest/actions/list-event-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/novacal/latest/actions/list-event-types?${params}`, {
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
      "color": "string",
      "description": "string",
      "duration": 1,
      "hidden_from_profile": true,
      "id": 1,
      "name": "Ava Chen",
      "slug": "string",
      "team_id": 1,
      "type": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Event type color. |
| `description` | string | Event type description. |
| `duration` | number | Duration in minutes. |
| `hidden_from_profile` | boolean | Whether the event type is hidden from the profile. |
| `id` | number | Event type ID. |
| `name` | string | Event type name. |
| `slug` | string | Event type slug. |
| `team_id` | number | Owning team ID. |
| `type` | string | Event type scheduling mode. |
| `user_id` | number | Owning user ID. |

## Native endpoint

Through the native Novacal API, this operation is `GET /v1/event-types` (base URL `https://api.novacal.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-types.md) for the provider-specific parameters and requirements.

