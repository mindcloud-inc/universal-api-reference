# ClickMeeting: List Conferences

Retrieves conferences from ClickMeeting by active or inactive status.

```
GET https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-conferences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-conferences?connectionId=$CONNECTION_ID&status=active" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "status": "active"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-conferences?${params}`, {
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
| `status` | list | yes | Choose whether to return active or inactive conference rooms. One of: `active`, `inactive`. Default: `active`. |
| `page` | number | no | Optional page number for inactive conference paging. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "embed_room_url": "https://example.com",
      "id": 1,
      "name": "Ava Chen",
      "permanent_room": true,
      "registration_enabled": 1,
      "room_type": "string",
      "room_url": "https://example.com",
      "status": "string",
      "timezone": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Conference creation timestamp. |
| `embed_room_url` | string | Embeddable conference room URL. |
| `id` | number | Conference room identifier. |
| `name` | string | Conference room name. |
| `permanent_room` | boolean | Whether the room is permanent. |
| `registration_enabled` | number | Registration toggle reported by the API. |
| `room_type` | string | Conference room type. |
| `room_url` | string | Conference room URL. |
| `status` | string | Conference room status. |
| `timezone` | string | Conference time zone. |
| `updated_at` | date | Conference update timestamp. |

## Native endpoint

Through the native ClickMeeting API, this operation is `GET conferences/{{status}}` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conferences.md) for the provider-specific parameters and requirements.

