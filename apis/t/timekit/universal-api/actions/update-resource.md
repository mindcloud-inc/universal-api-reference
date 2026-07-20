# Timekit: Update Resource

Updates an existing resource in Timekit.

```
PUT https://connect.mindcloud.co/v1/universal/timekit/latest/actions/update-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timekit/latest/actions/update-resource" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timekit/latest/actions/update-resource', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | no | First name of the resource. |
| `id` | string | yes | ID of the specific resource. |
| `lastName` | string | no | Last name of the resource. |
| `meta` | object | no | Metadata for the resource. |
| `password` | string | no | Password for the resource account. |
| `timezone` | string | no | Timezone of the resource. |

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

Through the native Timekit API, this operation is `PUT /resources/:id` (base URL `https://api.timekit.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-resource.md) for the provider-specific parameters and requirements.

