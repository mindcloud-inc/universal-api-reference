# Timekit: Create Resource

Creates a new resource in Timekit.

```
POST https://connect.mindcloud.co/v1/universal/timekit/latest/actions/create-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timekit/latest/actions/create-resource" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "timezone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timekit/latest/actions/create-resource', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "timezone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `availabilityConstraints[]` | array<object> | no | Resource-level availability constraints. |
| `email` | string | no | Email of the resource. |
| `firstName` | string | no | First name of the resource. |
| `image` | string | no | Image URL for the resource. |
| `lastName` | string | no | Last name of the resource. |
| `meta` | object | no | Metadata for the resource. |
| `name` | string | yes | Set the resource name. |
| `password` | string | no | Password for the resource account. |
| `timezone` | string | yes | Timezone of the resource. |

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

Through the native Timekit API, this operation is `POST /resources` (base URL `https://api.timekit.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-resource.md) for the provider-specific parameters and requirements.

