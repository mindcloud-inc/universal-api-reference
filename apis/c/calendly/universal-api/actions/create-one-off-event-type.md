# Calendly: Create One-Off Event Type

Creates a one-off event type in Calendly.

```
POST https://connect.mindcloud.co/v1/universal/calendly/latest/actions/create-one-off-event-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calendly/latest/actions/create-one-off-event-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "One-off Session",
  "host": "https://api.calendly.com/users/264e5a40-147f-45f9-a96c-a6f2f0a91dff",
  "duration": "30",
  "date_setting": {},
  "date_setting.type": "date_range",
  "date_setting.start_date": "2026-03-15",
  "date_setting.end_date": "2026-03-15"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calendly/latest/actions/create-one-off-event-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "One-off Session",
    "host": "https://api.calendly.com/users/264e5a40-147f-45f9-a96c-a6f2f0a91dff",
    "duration": "30",
    "date_setting": {},
    "date_setting.type": "date_range",
    "date_setting.start_date": "2026-03-15",
    "date_setting.end_date": "2026-03-15"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | One-off event type name. Default: `One-off Session`. |
| `host` | string | yes | Host URI (user URI). Default: `https://api.calendly.com/users/264e5a40-147f-45f9-a96c-a6f2f0a91dff`. |
| `duration` | number | yes | Duration in minutes. Default: `30`. |
| `timezone` | string | no | Event timezone. Default: `UTC`. |
| `date_setting` | object | yes |  |
| `date_setting.type` | string | yes | Date setting type for one-off event type. Default: `date_range`. |
| `date_setting.start_date` | date | yes | Date value when using a specific day. Default: `2026-03-15`. |
| `date_setting.end_date` | date | yes | Date range end date (YYYY-MM-DD). Default: `2026-03-15`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resource": {
        "active": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "duration": 1,
        "kind": "string",
        "locale": "string",
        "name": "Ava Chen",
        "profile": {
          "name": "Ava Chen",
          "owner": "string"
        },
        "schedulingUrl": "https://example.com",
        "secret": true,
        "slug": "string",
        "type": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "uri": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resource.active` | boolean | Whether the event type is active. |
| `resource.createdAt` | date | Creation timestamp. |
| `resource.duration` | number | Duration in minutes. |
| `resource.kind` | string | Scheduling kind. |
| `resource.locale` | string | Locale code. |
| `resource.name` | string | Event type name. |
| `resource.profile.name` | string | Profile display name. |
| `resource.profile.owner` | string | Profile owner URI. |
| `resource.schedulingUrl` | string | Public scheduling URL. |
| `resource.secret` | boolean | Whether it is a secret one-off type. |
| `resource.slug` | string | Slug for the event type. |
| `resource.type` | string | Event type category. |
| `resource.updatedAt` | date | Last update timestamp. |
| `resource.uri` | string | One-off event type URI. |

## Native endpoint

Through the native Calendly API, this operation is `POST /one_off_event_types` (base URL `https://api.calendly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-one-off-event-type.md) for the provider-specific parameters and requirements.

