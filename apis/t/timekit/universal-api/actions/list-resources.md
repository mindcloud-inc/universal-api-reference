# Timekit: List Resources

Lists all available resources in Timekit.

```
GET https://connect.mindcloud.co/v1/universal/timekit/latest/actions/list-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timekit/latest/actions/list-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timekit/latest/actions/list-resources?${params}`, {
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
      "api_token": "string",
      "calendars": [
        {
          "backgroundcolor": "string",
          "created_at": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "foregroundcolor": "string",
          "id": "string",
          "name": "Ava Chen",
          "provider": "string",
          "provider_access": "string",
          "provider_id": "string",
          "provider_primary": true,
          "provider_sync": true,
          "updated_at": "2026-05-07T12:00:00.000Z"
        }
      ],
      "conference_enabled": true,
      "conference_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "email_verified": "ava@example.com",
      "enabled_email_notification": true,
      "explicit_consent": "string",
      "first_name": "Ava",
      "id": "string",
      "image": "string",
      "last_name": "Chen",
      "meta": {
        "validatedAt": "2026-05-07T12:00:00.000Z",
        "wizardRun": "string"
      },
      "name": "Ava Chen",
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
| `api_token` | string |  |
| `calendars` | array<object> |  |
| `calendars[].backgroundcolor` | string |  |
| `calendars[].created_at` | date |  |
| `calendars[].description` | string |  |
| `calendars[].foregroundcolor` | string |  |
| `calendars[].id` | string |  |
| `calendars[].name` | string |  |
| `calendars[].provider` | string |  |
| `calendars[].provider_access` | string |  |
| `calendars[].provider_id` | string |  |
| `calendars[].provider_primary` | boolean |  |
| `calendars[].provider_sync` | boolean |  |
| `calendars[].updated_at` | date |  |
| `conference_enabled` | boolean |  |
| `conference_type` | string |  |
| `created_at` | date |  |
| `email` | string |  |
| `email_verified` | string |  |
| `enabled_email_notification` | boolean |  |
| `explicit_consent` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `image` | string |  |
| `last_name` | string |  |
| `meta.validatedAt` | date |  |
| `meta.wizardRun` | string |  |
| `name` | string |  |
| `timezone` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Timekit API, this operation is `GET /resources` (base URL `https://api.timekit.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-resources.md) for the provider-specific parameters and requirements.

